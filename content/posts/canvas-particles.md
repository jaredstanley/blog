---
title: Canvas Particles
description: This is a canvas experiment that turned out pretty
month: 05
day: 02
year: 2013
---
This is a canvas experiment that turned out pretty:

<br>

dust_result

 

<br>

I started with a 2-color black/white gif which gets loaded into a canvas and hidden.

<br>

Then i just have particles go to a point and then upon arrival choose a different point.

<br>

At each iteration i check the current pixel value; if it’s black the dot draws black; otherwise it chooses a color from within a range.

<br>

There is some inaccuracy when the colors are drawn; this is by design. I’m taking the previous x and y position and performing the calculations based on that. To remedy this you can just put the color-selection code after the point at which the x and y positions are set…i found this to be too precise, resulting in a boring visual.

<br>

### Performance

It runs awesome on Safari on iOS and on OSX. On Chrome on iOS it runs great, but on OSX it’s super-chuggy. I have it at ~100 particles so that it runs decent on Chrome; Safari can handle 300-600 particles easily.

<br>

I switched out the setInterval with the newer requestAnimationFrame – I noticed a little difference but it wasn’t a ton.

<br>

I could definitely optimize this more; in the future I’ll try the following:

<br>

- Put the source image pixel data into an array – the context.getImageData() is really processor intensive. I think putting it all into an array will reduce the load greatly. This would also eliminate the need for multiple canvases.

- Put the colors into an array – the random color is chosen from a range. It would make sense to just have a lookup table of a few colors and pull from there.  

- Use a better easing algorithm – this is just using the Xeno’s Paradox calculation…I haven’t optimized any of that but I think that could be done in a less taxing way.

- It would be cool to have this pull from different images after a time, the result being a gradual transition from image one to image 2.

- It would also be cool to try 3-color images, 4-color images etc.


<br>
