---
title: Tweening a vector path in SVG
description: I started looking at ways to tween a path, tried to do it with straight svg so I could spend a little time with the format.
month: 05
day: 15
year: 2013
---

I started looking at ways to tween a path, tried to do it with straight svg so I could spend a little time with the format.

I got it working. Sort of. Click to see the result:

svgtween

What I learned:
It IS possible to tween a path with svg(like a shape tween in flash), but it’s severely limited.

First of all, if you’re going to animate properties, SVG is great. x/y position, rotation, etc. very straightforward and there are plenty of good examples online. Many of the popular SVG libraries such as RaphaelJS utilize this and can be very powerful. Likewise animation of these objects ALONG a path is also very easy and straightforward.

To animate or tween an actual path is different. You must first get all the points into the xml structure that SVG uses(you can save in illustrator/many other programs), and put them in a ‘from’ or ‘to’ attribute in an < animation > tag. Here’s a sample ‘from’ attribute:

from=”M12.309,198.552c0-56.941,17.208-101.701,51.626-134.277c34.417-32.573,81.855-48.863,142.316-48.863 c60.124,0,107.397,16.247,141.814,48.737c34.418,32.494,51.626,77.294,51.626,134.403c0,56.944-17.169,101.618-51.5,134.026 c-34.334,32.408-81.647,48.612-141.94,48.612c-60.461,0-107.899-16.243-142.316-48.737 C29.517,299.963,12.309,255.328,12.309,198.552z”

This is a version of the SMIL specification for animation. The string is full of line commands specific to this language. note the ‘M’ at the beginning, followed by two values 12.309 and 198.552 – this is the ‘MoveTo’ command with an x and y value. Next there’s a ‘c’ which is a ‘Curve’ command; bezier and cubic curves are supported. At the end there’s a ‘z’ which serves as a closing indicator; the z command must always be the final character in the string. More info on all these commands used on the < path > element can be found here.

The big bummer is this:

Currently you have to use the same number of vertices in both path-elements, and they have to be of the same type and appear in the same order in the other path-description. You should also orient both polygons in the same direction (left-right and right-left would produce unwanted results).

So as you can see in my example it IS possible, but you need to plan it out so that you create shape A’s path and shape B’s path in the exact same way with identical curve types, points, etc.

Here’s the workflow I found:

(FYI in the above example I have two svgs on the page that are both set as masks of an image; the one on the right is the one that animates)

I created one shape in illustrator, the more complex shape.
I duplicated the complex shape and moved the points to create a second shape, careful not to add vertices or change from bezier to linear curve type etc – ONLY MOVE THE POINTS (just use the direct selection tool and move singular points to be safe)
fyi to confirm point count you can select the path, then go path>simplify and it will show you current point count on that path…
I save that svg file, then copy/paste those paths into another svg with the animation information.
NOTE: the paths are placed within an element in the svg file that corresponds to the layer name that it’s on in illustrator. If you keep both shapes on different layers in illustrator and name them clearly it will help keep your svg files organized.
NOTE #2: If you create your shape and it’s very simple, ie only straight lines, it will likely get saved as a _polygon instead of a _path which animate in a completely different way than paths, so I recommend adding a bezier handle to at least a single point(and the identical corresponding point in the second shape).
 Other Libraries:
I’ve seen other libraries that possibly solve this, but I haven’t spent any time exploring them.

This one looks interesting: http://jonobr1.github.io/two.js/, but it says it’s ‘renderer-agnostic’ which leads me to believe that they’re just using canvas in those instances. Still, that’s potentially a solid option.

 