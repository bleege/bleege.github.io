---
layout: post
title: OS X Yosemite Display Grays Out
date: '2014-10-26T12:34:00-05:00'
tags:
- apple
- osx
- os x yosemite
- displaypolicyd
tumblr_url: http://bleege.tumblr.com/post/101008783822/os-x-yosemite-display-grays-out
---
[OS X Yosemite Display Grays Out](https://discussions.apple.com/thread/6624349)

I’ve been running OS X Yosemite on my 2011 iMac for a few weeks now.  I really like it as it’s seems to have breathed some life back into the old hardware.  That said, I have had several times where the display will just gray out or stop working.  Trying to reboot only starts an infinite loop of reboots as it makes it halfway through startup, stalls, and then automatically reboots itself.  After MANY hours of searching, the only solution that I’ve found is to boot into Recovery Mode and use the Disk Utility to Verify and Repair Permissions.

This [Apple Support Forum link](https://discussions.apple.com/thread/6624349) provides a shell script that you can use to automatically fix the problem upon login.  More importantly though it seems to confirm that it’s actually consistently an issues with _displaypolicyd_
