---
layout: post
title: Making things move
date: 2016-07-08 19:44:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - intro
---

This script does next to nothing. It shows the basic layout of a sketch. A setup function, and a draw function. We [create a canvas](http://p5js.org/reference/#/p5/createCanvas) with a width of 500 pixels and a height of 200 pixels, and we set its background color to be gray. Each sketch will have a canvas in which it operates.

`canvas = createCanvas(500, 200);` creates an object called `canvas` which is a canvas.


{% include code-sketch-view.html whichSketch="2.1" %}


The next line: `background(200);` gives a background color, given by then number 200, which means make it gray. (0 would be black, 255 is white)

Here it is:

{% assign toshow = site.p5scripts | where: "refno", "2.1" %}

<iframe class="tut-canvas" src="{{site.baseurl}}{{toshow[0].url}}.html" width="500" height="200"></iframe>

More: learn about colors in p5 here: [Color Ref](http://p5js.org/reference/#/p5/color)

Now, let's put something in the draw function. We'll draw an [ellipse](http://p5js.org/reference/#/p5/ellipse) and put it in the center of the canvas. The `ellipse` function take 4 arguments: the first two numbers indicate its x and y positions. The second two are its horizontal and vertical radii. By saying: `width/2`, we are indicating to put the ellipse halfway across the `width` of the canvas. We could have also said 250, since the canvas is 500 pixels wide.

{% include code-sketch-view.html whichSketch="2.2" %}


Now, we would like to incorporate some motion in our sketch. We'll do this by adding a small number to the x position of the ellipse every frame. We'll call that small number `dx` and set it equal to `1` (on line 3).

We'll also make some variable to store the x and y positions: `xpos` and `ypos`. We set `ypos` equal to `height/2`, which means it will always stay in the middle of the canvas, vertically. But the `xpos` variable will change every frame. Line 11 says: `xpos = xpos + dx`. Since `dx` is equal to `1`, that means the x-position value will increase by one unit every time the draw function is called.



Here is the sketch. **Note: you might need to click the refresh sketch button**


{% include code-sketch-view.html whichSketch="2.3" %}

Things to play with:

- change the _speed_ of the ball
- change the direction of motion
- change the y-position also

We don't want to loose our happy little ellipse when it gets to the other end. Here's a way to have it start over on its journey when it reaches the opposite side. We can use an *if statement*. This basically says, if this relation is met (i.e if the x-position is greater than the width of the canvas, the reset the x position to zero) then do something:

`if (xpos > width) { xpos=0; }`

{% include code-sketch-view.html whichSketch="2.4" %}
