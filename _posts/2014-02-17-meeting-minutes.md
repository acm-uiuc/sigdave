---
layout: default
title: Turret integration
---

Today we (Zane and I) added turrent integration to the DJ Roomba stack.
I also finished the diagram (using the [diagram](http://projects.haskell.org/diagrams/)  dsl).

The wiimote works, however it doesn't register events using the linux stack (using cwiid).
That said it has a python2 api. We're going to try getting it to register as a joystick, but if we will write a joystick daemon using the python2 cwiid library.

Marcell V.C
