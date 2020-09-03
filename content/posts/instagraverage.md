---
title: Instagraverage
description: i’ve loved Jason Salavon’s work ever since I saw this
month: 08
day: 06
year: 2012
---

UPDATE: this project morphed into what we called Metagramme, info [found here](https://jareds.myportfolio.com/metagramme)

<br>

i’ve loved [Jason Salavon’s](http://www.salavon.com/) work ever since I saw this:

<br>

![img](/playby.png)

<br>

It’s a mathematical average of every centerfold from playboy for 10 years.

<br>

Here’s another one of 114 homes for sale in the Dallas/Ft. Worth area:

<br>

![img](/dallas.png)

<br>

I decided to try to mimic this process and average out all of my instagram images.
The images above work because they have similar compositions; instagram images all have identical aspect ratios but there is no pattern to the compositions other than maybe darkened edges…

<br>

For now I’m limited by the Instagram API (which paginates the results at 60 images) due to a bug in my code(I can’t parse the JSON when the second call is returned for some reason) so these are just the most recent 60 images.
Here’s my first attempt at a proof-of-concept – here are my 60 most recent instagram(@j_red) images averaged out:

<br>



You can see the borders from snapseed in there, and the diagonal lines that look like a huge fingerprint are from a contrasty image of tyler durden on the tv i shot in the dark.
As expected the colors average out to a contour-less image, but it’s actually pretty to look at.

<br>

Here is my wife’s account(liz_stan):

<br>


next I tried images via google’s image search.

here is the average composite of the first 200 image results for ‘eiffel tower':



<br>

the average composite of the first 200 images from the query  ‘golden gate bridge':



<br>

and this is the first 200 for ‘tree':


<br>


The images are all aligned top-left (which is why they run out of pixel data on the bottom-right) but even with vertical and horizontal images you can get a general idea of what the item is.

<br>

I’m working on an application which i’m calling ‘instagraverage’, which is a terrible name, that lets you do your own account; I was pleased with the google results as well so I may add that.

 

