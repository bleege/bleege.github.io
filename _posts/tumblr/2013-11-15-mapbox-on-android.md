---
layout: post
title: MapBox On Android
date: '2013-11-15T11:13:00-06:00'
tags:
- mapbox
- android
- openstreetmap
- opensource
- osmdroid
tumblr_url: http://bleege.tumblr.com/post/67067786840/mapbox-on-android
---
<!--excerpt.start-->
I’m a big fan of the work that [MapBox](https://www.mapbox.com) has done with [OpenStreetMap](https://www.openstreetmap.org/) and the great [open source tools](https://www.mapbox.com/developers/) that they provide for building custom maps.
<!--excerpt.end-->

However after searching the Web and talking with MapBox Engineers I discovered that there is no support for Android, [nor are there any plans to do so](https://www.mapbox.com/help/#android-sdk).  This bugged me as I want to make use of their maps on some Android projects, so I did some research and built a solution.

My original proof of concept project, called [BikeMapBox](https://github.com/bleege/BikeMapBox), is available on GitHub, but to make it easier for others who are looking for a solution too I [worked](https://code.google.com/archive/p/osmdroid/issues/491) with the [OSMDroid](https://code.google.com/archive/p/osmdroid/) team to have it included in that project.  It’ll be available in the next OSMDroid official release (it’s already in the SNAPSHOT builds on Maven Central), but if you’d like to use it now you can [download the code](https://code.google.com/archive/p/osmdroid/source) and include it in your project’s source code.


Usage is pretty straightforward.

Add a MapView to your layout.xml file

{% highlight xml %}
<org.osmdroid.views.MapView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
{% endhighlight %}

Add your MapBox Map Id to AndroidManifest.xml

{% highlight xml %}
<meta-data android:name="MAPBOX_MAPID" android:value="example.map-3a5gfw2p"/>
{% endhighlight %}

Create And Associate the MapBoxTileSource with your MapView in your Activity

{% highlight java %}
MapBoxTileSource.retrieveMapBoxMapId(Context context);
MapBoxTileSource mapBoxTileSource = new MapBoxTileSource();

MapView mapView = (MapView)findViewById(R.id.mapview);
mapView.setTileSource(mapBoxTileSource);
{% endhighlight %}
