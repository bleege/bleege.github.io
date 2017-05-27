---
layout: post
title: Hey Mapbox How Do I Get To...
date: '2016-01-30T21:45:40-06:00'
tags:
- mapbox
- voice
- android
- directions
- geocoding
tumblr_url: http://bleege.tumblr.com/post/138384486952/hey-mapbox-how-do-i-get-to
---
Earlier this month we released Android wrapper libraries for the Mapbox [Geocoding](https://www.mapbox.com/blog/android-geocoder-library/) and [Directions](https://www.mapbox.com/blog/android-directions-library/) API services to make adding Geocoding and Directions in your Android apps much easier.  Naturally I wanted to do just that so I built a demo app called [Go Where I Say](https://github.com/bleege/GoWhereISay) that uses Android’s stock Speech To Text API to generate Directions based on voice commands. Did I mention that Google Play Services is NOT required?  In other words it’s not only possible but it’s super easy to ask Mapbox for AND get directions to locations by using your voice inside your own apps without having to (rely on or) say “Hey Siri” or “Ok Google”.  Checkout out the [source code](https://github.com/bleege/GoWhereISay) to see for yourself how to add this to your own apps.

![](/tumblr_files/example-screen-recording.gif)