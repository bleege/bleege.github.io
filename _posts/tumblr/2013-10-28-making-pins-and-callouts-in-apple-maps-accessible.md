---
layout: post
title: Making Pins and Callouts in Apple Maps Accessible
date: '2013-10-28T12:27:53-05:00'
tags:
- accessibility
- ios
- maps
- mapkit
- mkmapview
- apple
- apple maps
tumblr_url: http://bleege.tumblr.com/post/65348339000/making-pins-and-callouts-in-apple-maps-accessible
---
<!--excerpt.start-->
Pins (aka location markers) and Callouts on instances of MKMapView are not automatically accessible to blind users via iOS’s VoiceOver feature.  The impact of this is that while blind users may be able to load your app’s map they won’t be able to find any of the content that you’ve placed on the map.  Thankfully, there’s an easy fix for this using the stock Accessibility framework that Apple provides in iOS.
<!--excerpt.end-->

Update your MKMapViewDelegate’s callOut and set annotationView objects to be accessible.

{% highlight objective-c %}

- (MKAnnotationView *)mapView:(MKMapView *)mv viewForAnnotation:(id )annotation
{
	NSString *identifier = @"PINIDENTIFIER";
	MKPinAnnotationView *annotationView = (MKPinAnnotationView *)[mapView dequeueReusableAnnotationViewWithIdentifier:identifier];
	if (annotationView == nil)
	{
		annotationView = [[MKPinAnnotationView alloc] initWithAnnotation:annotation reuseIdentifier:identifier];
		annotationView.canShowCallout = true;
		UIButton *callOut = [UIButton buttonWithType:UIButtonTypeDetailDisclosure];
		[callOut setAccessibilityValue:@"Tap To Perform Some Action"];
		annotationView.rightCalloutAccessoryView = callOut;
		[annotationView setIsAccessibilityElement:YES];
		annotationView.accessibilityValue = @"Tap this pin show a callout with more information.";
	}
	return annotationView;
}

{% endhighlight %}

Make sure any UIView that the MKMapView may be contained in the XIB has it’s accessibility option set to NO.  Not doing so will cause the map view to be accessible, when it’s only the pins and callouts that are desired.
