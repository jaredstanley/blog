---
title: tree ring - processing
description: My wife received this book in the mail
month: 06
day: 18
year: 2012
---

My wife received this book in the mail:

![tree book](/treebook.jpg)

It’s beautiful, with awesome images of tree rings; I thought I’d try to recreate a tree’s growth procedurally.

<br>

Here’s my first attempt at recreating a tree ring:

<br>



I followed these steps:

<br>

- -get points distributed evenly around the circumference of a circle

- -get the curveVertex() method in processing to work. If you just loop through the points, the first and last points have no lines drawn – this is because curveVertex() requires a minimum of four points; you just need to check if it’s first or last and then duplicate current point on true.

- -i wanted some variance, so i added a random amplitude var to the equation. Adding this randomly didn’t quite work; a tree seems to have consistent inconsistencies – a funny growth or infection or foreign object etc. To achieve this I just assigned a the randomness to the point when I created it, that way it stays consistent every time it’s referenced.


<br>


it’s a good first step, maybe i’ll work on it more soon.

<br>
