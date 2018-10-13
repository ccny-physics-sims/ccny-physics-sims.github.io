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

What is p5.js and what can it do?

## 1. The basics

P5.js is a javascript library that allows us to draw and animate things on webpages. Think of the webpage as a canvas - p5.js contains a bunch of commands like `ellipse()` and `line()` and `rotate()` that will make shapes and modify them to create interactive animations or visualizations.

We'll call the set of commands we write a _sketch_.

Here is a very simple one that makes a blue canvas and draws a circle on it. (Press the "play sketch" button below the box to run the sketch.)

{% include code-sketch-view.html whichSketch="good.1" %}

You can see there are two main sections to the sketch: the `setup` and the `draw`. Things in the setup get done once, at the beginning, and things in the draw part get done over and over, about 30 times a second. Here's an example where we draw circles over and over again at random locations.

`ellipse(random(width),random(height),30)`

means to place an ellipse at a random position between zero and the width of the canvas (in the x), and zero and the height (in the y) and make its radius equal to 30 pixels. `ellipse()` is an example of a built in function or command in p5. (To learn how to use it, you can always look at the [reference documentation](https://p5js.org/reference/#/p5/ellipse) for p5.js.)

{% include code-sketch-view.html whichSketch="good.2" %}

That summarizes the basic outline of a sketch. Some things are found in most sketches:

`createCanvas(w,h)` will create the canvas that we draw on.

https://p5js.org/reference/#/p5/createCanvas

`background(color)` will make the background a certain color. Here we can see how moving the `background()` command to the draw section will change our set of random orange balls. Now the background is drawn over and over, just before the orange ball, so it effectively erases the previous ball.

https://p5js.org/reference/#/p5/background

{% include code-sketch-view.html whichSketch="good.3" %}

## 2. Mathy things

Since these are computer programs, we would expect them to be able to do mathy type things. This sketch calculates the square root of two and displays it using the `text()` function.

{% include code-sketch-view.html whichSketch="good.4" %}

### Trigonometry

Trigonometry is very useful and easy to do in p5.

Here we can use the arctan (`atan2(opp,adj)`) to find the angle between the line and the horizontal axis. We'll also round it to 2 decimal points (`toFixed(2)`) and add the word 'degrees' after it. Now we can label things!

{% include code-sketch-view.html whichSketch="good.5" %}

## 3. Interactions

The previous sketch introduced something else, user interactions. The sketch looked to see where the mouse was and used that to draw the line

`line(0,0,mouseX,mouseY)`

means to draw a line starting at x = 0 and y = 0 and continue to x = horizontal mouse position, and y = vertical mouse position. Now we can input from the user and change our sketch to deal with that. There are many ways of interacting with web pages.

Sliders are good ways:

`createSlider(low,hight,initial,increment)`

{% include code-sketch-view.html whichSketch="good.6" %}

That's a quick overview of the very basics of p5. Here is another tutorial that gets a little deeper:

[part 2]({{site.baseurl}}/tutorials/things-p5-is-good-at-pt2)
