---
layout: post
title:  Getting Started with a p5 sketch
date:   2016-07-05 19:44:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - intro
---

{{site.p5scripts | where: "refno", "1.1"}}

The quickest way to get started building a sim will be to download the p5 editor app. This app lets you build quick sims and see them in action without having to set up much.

Download it [here](https://p5js.org/download/#editor).

Upon opening the app, you will see a window like this:

![p5 editor window]({{site.baseurl}}/post-imgs/p5-window.jpg)

Press the play button and a small window will pop up that is all white. This is your canvas being drawn. It's not very interesting because there is nothing to be drawn.

In the coding window, you will see two functions: `setup()` and  `draw()`. These functions are the most basic elements of a p5 sketch.

The `setup()` function is called once in the beginning, when you press the play button. Then, the `draw()` function is called over and over again, about 30 times a second.

So, let's start by putting something in the setup function:

{% assign toshow = site.p5scripts | where: "refno", "1.1" %}

```javascript
{{toshow[0] | remove: '<script>' | remove: '</script>'  }}
```

I put in a command to draw an ellipse. Inside the parenthesis for this command are 4 *arguments*. The indicate where the ellipse should be, and how big it should be. So, this ellipse will be located at `x=10` and `y=30` and it will have a horizontal diameter of `20px` and a vertical diameter of `40px`.


 <iframe class="tut-canvas" src="{{site.baseurl}}{{toshow[0].url}}.html" width="100" height="100"></iframe>

Congrats! You made an ellipse. However, it doesn't do anything.

So, let's put the ellipse command in the `draw()` function instead. This means it will get repeated about 30 times a second (depending on the speed of the computer).

{% assign toshow = site.p5scripts | where: "refno", "1.2" %}

```javascript
{{toshow[0] | remove: '<script>' | remove: '</script>'  }}
```

Notice, I also added a small random number to each of the position arguments: `50+random(-5,5)`. This means that every time the draw function is called, it will pick a new random number (between -5 and +5) to add to the original position. So, we expect a jittery, nervous looking ellipse on our canvas.

{% assign toshow = site.p5scripts | where: "refno", "1.2" %}

 <iframe class="tut-canvas"  src="{{site.baseurl}}{{toshow[0].url}}.html" width="100" height="100"></iframe>

 That should be enough to spark some interest. Maybe you're wondering: _are there other shapes?_ For sure. You'll need to consult the reference docs to learn how they work.

 Link to p5.js [reference docs](http://p5js.org/reference/#group-Shape)
