---
layout: post
title:  "Soldering Saturday - Meeting Minutes"
---

## DJ Roomba ##
- So midway through soldering the leads on the LED ropes, we realized that we needed variable length leads (because some would be higher up that others).

We ended up with the following formulation:

{% highlight python %}
height = 48 # sonotube unit: inches
width = 1/4 # led rope unit: inches/rope
num_ropes = 32 # unit: rope
spacing = height/number - width # unit: inches/rope
buffer = 1 # unit: inch
lengths = map(lambda n: buffer + spacing*n, range(0, num_ropes))
{% endhighlight %}

- We also decided to use a common ground rail to remove excess wires

## Turret ##
- We tested the code at https://github.com/nmilford/stormLauncher and found it worked on Linux
- The usb camera registers properly on Linux
- The turret itself is just 1 way usb serial commands enumerated in the code.
- For integrating into DJ-Roomba:
-- Camera will define a sensor daemon that publishs its results
-- Turrent will define another controller to publish to

## Future Goals ##
- Need order bluetooth dongle for wiimote control
- DJ Roomba specific stuff is being moved to Saturdays
- Take pictures during meetings for easier documentation
