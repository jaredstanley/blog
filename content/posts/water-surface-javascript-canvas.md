---
title: water surface in javascript and canvas
description: We were talking about physics libraries and water and performance at work, I decided to mess around with that.
---



![test image](/grad.png)

We were talking about physics libraries and water and performance at work, I decided to mess around with that.

I have a single target point that oscillates with increasing velocity, then it dampens back down.

The points to the right of the target point all tie into their previous partner’s position at a consistent percentage, making the gelatinous or bendy effect; it looks like a wand waving or something.

The points to the left of the target point all tie into their next partner’s position, then have a decay added in, resulting in what looks like decaying waves.

The algorithm is kind of hacked together but this is straightforward math, I often use it in after effects expressions etc – I’m sure this could be optimized quite a bit.