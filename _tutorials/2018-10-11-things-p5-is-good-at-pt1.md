---
layout: post
title: Things p5.js is good at, part 1.
date: 2018-10-11 9:44:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - intro
summary: What are some easy things to do with p5 and astronomy or physics?
---

Let's look at some things that are both easy to do in p5.js and are potentially useful for physics and astronomy sims.

## 1. Changing the size of things

Here we see a circle that is located at the center (`x = width/2` and `y=height/2`). Its radius is set by the third argument: `sin(theta)`. `theta` is a variable that will change every frame, as indicated by the line:

`theta += 0.001`

which increments theta by 0.01 about 30 times per second. (every time the draw function repeats)

{% include code-sketch-view.html whichSketch="good.1" %}

You could also change the size based on user input. Here is a circle hooked up to a slider:

{% include code-sketch-view.html whichSketch="good.2" %}

## 2. Making things move

Since shapes and added objects will need positions, we can keep changing them all the time, which is just another way of saying the thing is moving. Now, instead of changing the radius argument of the `ellipse` function, we'll change the vertical position: `y = height/2 + 30*sin(theta)`. Again, we'll change theta by 1 every frame.

{% include code-sketch-view.html whichSketch="good.3" %}

And of course, this change could be effected by user input too:

{% include code-sketch-view.html whichSketch="good.4" %}

Naturally, we can combine these things into a single sketch:

{% include code-sketch-view.html whichSketch="good.5" %}

### another way to move things:

We can also make things change position by using the `translate(∆x,∆y)` function. This simply *translates* the position of everything below it in the draw routine. This time we'll move a rectangle (`rect()`).

{% include code-sketch-view.html whichSketch="good.6" %}

Similar to translate, is the `rotate()` function. This will rotate the object. Here we translate the object to the center

`x = width/2` and `y = height/2`

Then rotate it by a constantly increate `theta` value.

{% include code-sketch-view.html whichSketch="good.7" %}

Note the the order of `translate` and `rotate` makes a difference. This sketch below will rotate it, then translate, which effectively changes the center of rotation.

{% include code-sketch-view.html whichSketch="good.8" %}

## 3. Doing things over and over

Perhaps the most useful feature of using computers is that they are happy doing the same thing over and over. So, let's say we wanted to make many things, all doing similar, but slightly different actions. This sketch is structure to

  a) create a class called makeABall() (think of it like a collections of [function]({{site.baseurl}}/quick-tips/about-functions) )

  b) repeatedly create instances of this class and store them in an array (this uses a `for` loop)

  c) update the array and in doing so, update each of the balls.

{% include code-sketch-view.html whichSketch="good.9" %}
