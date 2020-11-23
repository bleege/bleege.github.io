---
layout: post
title: Making Location Edits To Apple Maps
date: 2018-01-29
featured: true
image: images/20180129/3.png
categories: [ Apple, Maps, Data ]
tags:
- apple
- apple-maps
- macos
- iphone
- ios
- maps
- data
- photos
- travel
- geotag
- geocoding
- copenhagen
- denmark
---

_tl;dr: Apple accepts location data additions and edits for Apple Maps via macOS Maps app._

<!--excerpt.start-->
As a traveler one of my favorite features about [macOS Photos](https://www.apple.com/macos/photos/) app is the map view that displays the location of each of my photos.  I love how this helps me remember my past travels as well as provides inspiration for places I have yet to visit.  Recently I imported some travel photos that did not have geolocation information needed to power the map display.  In order to get these photos to display on the map I had to geocode each photo.  While doing so I discovered several locations that Apple Maps didn't currently have.  macOS Photos's map works just fine with raw latitude / longitude coordinates for the photos but Apple Maps is much richer for all of us to have the locations labeled.  Thankfully Apple has a way to do this.
<!--excerpt.end-->

#### Søfartsmonumentet

One such location is the [Søfartsmonumentet](https://bibliotek.kk.dk/ting/object/159004-lokalbibl%3A93057333) in Copenhagen, Denmark.  It's a memorial built after World War I and features the [Greek goddess Nike](https://en.wikipedia.org/wiki/Nike_(mythology)).  It is located near the more famous Little Mermaid statue on the harbor.

<img src="/images/20180129/søfartsmonumentet.jpg" alt="Søfartsmonumentet"/>

#### Adding The Location

The first thing to do is to find and then mark the location on the map.  This is done via Control clicking on the point where the new location should appear.

<img src="/images/20180129/2.png" alt="Drop Pin"/>
_Drop Pin_

<img src="/images/20180129/3.png" alt="Marked Location"/>
_Marked Location_

#### Access To Location Data Editor

From the new pin tap the Info button to display the information Popover.  The "Report Issue" button is located at the bottom of the Popover and is what opens the location data editor.

<img src="/images/20180129/4.png" alt="Information Popover"/>
_Information Popover_

<img src="/images/20180129/5.png" alt="Report Issue Button"/>
_Open Location Data Editor via Report Issue button_


#### Create The Location Edits

From the location data editor sheet are options available for creating the location edits.  In this case "Add A Place" is selected and the subsequent step by step workflow is followed through to it's conclusion... Send to Apple!

<img src="/images/20180129/6.png" alt="Location Data Editor Sheet"/>
_Location Data Editor Sheet_

<img src="/images/20180129/9.png" alt="Add Location Editor Final Step"/>
_Add Location Editor Final Step_

#### Follow Up

Apple then usually takes about a week to review submissions and if they accept them then sends a notification to you via your Apple ID connected devices.  From there I've noticed that it usually takes another couple of weeks before the basemap is updated and shows the location.

<img src="/images/20180129/10.png" alt="Newly Added Location Popover"/>
_Newly Added Location Popover_

<img src="/images/20180129/11.png" alt="Newly Added Location On Basemap"/>
_Newly Added Location On Basemap_


Happy Mapping!


