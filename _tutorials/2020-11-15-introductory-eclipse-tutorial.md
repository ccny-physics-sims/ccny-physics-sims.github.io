---
layout: post
title: Let's make a solar eclipse
date: 2020-11-15 10:51:00 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - astronomy
summary: An introductory p5 tutorial that will produce a little solar eclipse simulator
---

## Getting Started

We'd like to make an interactive simulation that shows a solar eclipse, i.e. when the moon passes in front of the sun. We'll use p5.js to do this. So, if you're just starting out, in another browser window, head on over to the [p5.editor website](https://editor.p5js.org/). If you're already familiar with the p5 environment, then keep on reading and you can build it in your own editor.

This is our very initial sketch. It does nothing other than make a `canvas` and paint it gray.

{% include code-sketch-view.html whichSketch="eclipse.1" %}

## We need some sunlight in this room.

Next we can add a sun. This is just a yellow circle which we can draw by using the `circle()` function:

`circle(0,0,80)`

The first two zeros tell the circle to position itself at the `x=0` and `y=0` coordinates, which in a canvas like this, is located at the top left. The third parameter is the diameter, in this case 80 pixels.

The `fill()` function says what color the circle should be. How about yellow?

`fill('yellow')`

{% include code-sketch-view.html whichSketch="eclipse.2" %}

And, we should put the sun in the center of the frame. One way to do this would be to change the two zeros in the `circle` function to `200, 200` so that it's in the middle of the 400 pixel square canvas. But, there's a better way. We can use `translate()` to move the origin of the frame to the center:

`translate(width/2, height/2)`

Now, the sun should be in the middle of everything since it's been moved by an amount equal to half the width, in the x direction, and half the height in the y direction (positive is down in this situation )

{% include code-sketch-view.html whichSketch="eclipse.3" %}

## But where is the moon?

Let's put a moon in there. It should be circle the same size as the sun (what an amazing coincidence right?). And we'll just place it a little to the left of the sun, so it gets a position of `x = -40, y = 0`

`circle(-40,0,80)`

{% include code-sketch-view.html whichSketch="eclipse.4" %}

## Doesn't the moon move?

Now comes the fun part. We'll add some interactivity and make a slider controller that will move the moon.

We can do this by adding an element called a range slider in the `setup()` function:

`slider = createSlider(-80, 80, -80);`

`slider.position(10, 10);`

And then in the `draw()` function, we'll add a way to retrieve the value of the slider:

`val = slider.value();`

I've already set the slider up so that's its range of values is appropriate. It's minimum value is `-80`, the maximum is `+80`, and the initial value is `-80`

i.e. `createSlider(minimum, maximum, initial)`

Now, put that variable called `val` into the x position of the moon circle:

And here it is, a movable moon that passes in front of the sun:

{% include code-sketch-view.html whichSketch="eclipse.5" %}

## I want more fancy

Here's a link to the p5.editor that has this sketch included so that you can use it as a starting point:

[Moon Moves Across the Sun](https://editor.p5js.org/jhedberg/sketches/i-Hrv4_BY)

There is a lot more to do to improve this simulation. If you've seen a total eclipse, you might remember that the sky darkens and stars appear. Here we've added these features to the simulation:

- blue sky
- moon is not visible until it crosses the sun
- stars appear at totality

We'll do a follow up tutorial that explores these more advanced features.

{% include code-sketch-view.html whichSketch="eclipse.6" %}
