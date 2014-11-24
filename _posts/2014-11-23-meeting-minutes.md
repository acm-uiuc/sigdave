---
title: Food Button Status Report
layout: post
---

# Button Works

So, we are super close to being able to ship the food button.
During the last meeting Sam and I were able to test usage of 
the button to toggle a file descriptor on the beagle bone. It
uses the sysfs gpio interface which makes it pretty language 
agnostic to use.

# 3d Model done and submitted

Chris Han created a 3d model to house the foodbutton electronics.

Take a look!

- [https://github.com/acm-uiuc/Food-Button/blob/master/lid.stl](https://github.com/acm-uiuc/Food-Button/blob/master/lid.stl)
- [https://github.com/acm-uiuc/Food-Button/blob/master/box.stl](https://github.com/acm-uiuc/Food-Button/blob/master/box.stl)

I also just submitted the jobs for the ACM 3d printer.

# Ethernet port access

We've gained access to Ethernet ports for the beagle bones.

We may explore wifi enabled setups in the future, but this allows
us to install packages and upload the images to twitter.

# Trouble in Paradise

ffmpeg seems to hang when we try to capture images from the webcam.
We're going to explore using the same version I used to test the feature.
If not, we may switch to an alternative method of capturing from the webcam.

- Marcell V.C
