---
layout: post
title: Using colors in P5.js
date: 2018-10-26 6:00:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - colors
summary: Little tips for colors in P5
---

## Method 1. You know my name...

There are many ways of telling a computer to draw a particular color. P5.js has a number of these built in. The simplest is to use the predefined colors like `'red'` or `'blue'`. Those keywords are predifined to create colors that we know as red or blue. There are also more [exotic colors](https://htmlcolorcodes.com/color-names/) predefined like `'hotpink'` or `'chartreuse'`. Here's a little sketch that makes the background the color of moccasins: `background(moccasin)`. (My moccasins are a little darker I think, but you get the idea)

{% include code-sketch-view.html whichSketch="colors.1" %}

## Method 2. It's just gray out today

Before getting into colors, let's just start with shades of gray. P5 can display 255 different grays easily, just pick a number between 0 and 255, and that will give you a corresponding gray. (0 is black, 255 is white) This little sketch continuously sets the background to a different shade of gray by using a sine function. The color of the text is set by the cosine, since we always want the text to be different than the background.

{% include code-sketch-view.html whichSketch="colors.2" %}


## Method 3. Roy G. Biv

If you need finer control of things, and don't want to be limited by the set of colors defined by some folks who don't see the world like you do, then you can define your own color by setting the amount of Red, Green, and Blue that will be displayed. If you were to look at your monitor with a microscope (go ahead, do it!), you'd see a array of little rectangles that are either Red, Green, or Blue. The amount of each one determines what color the screen is showing.


<figure class="figure col-lg-6 col-sm-12 float-left">
<img class="figure-img img-fluid rounded" src="{{site.baseurl}}/post-imgs/rgb.jpg" alt="rgb" />
  <figcaption class="figure-caption">Magnified image of a computer screen</figcaption>
</figure>

So, by telling P5 to display a certain amount of Red, Green, and Blue, we can control the color. The range for each value usually is set between 0 and 255, which 255 being the most. This is the default format in P5 so if you write:

`color(255,50,50)`

this will create a color with mostly red, and a little green and blue in it.

{% include code-sketch-view.html whichSketch="colors.3" %}

We can programmatically adjust the RGB values, depending on something, like a user input or position or whatever you want. For example, a slider could be used to adjust the red value.

{% include code-sketch-view.html whichSketch="colors.4" %}

### strings

We can also use strings (variables defined using quotes: `'string'`), rather than numeric values to define the colors. The following two lines will do exactly the same thing:

`c = color('rgb(0%, 0%, 100%)')`

`c = color(0,0,255)`


{% include code-sketch-view.html whichSketch="colors.5" %}


## Method 4. Other color schemes

The RGB color model is very useful and great for come applications. However, there are other ways to define a particular color, for example, using the Hue, Saturation, and Lightness, or HSL. Some rough definitions:

1. Hue will set the basic color along the spectrum, from 0 to 360 where 0 is red, 180 is bluegreen, and 360 is back to red.
2. Saturation ranges from 0 to 100% and determines how much color is in the presentation.
3. Lightness also ranges from 0 to 100% and sets the brightness of the color shown.

The HSL model is useful when you want to keep the same hue (color), but change the other parameters, or smoothly range through a spectrum. Here's a little wheel that shows the changing hue value

{% include code-sketch-view.html whichSketch="colors.6" %}

Here are some lines that slowly change either the saturation or the lightness as a function of their position in the canvas. The upper half all have the same hue (blue) and saturation (100%), which the lines on the lower half have the same hue and lightness.

{% include code-sketch-view.html whichSketch="colors.7" %}

This can be useful for suggesting two things, like lines in a graph, are related, but different.

## Method 5. By wavelength

As physicists, we consider color to just be defined by the wavelength of the light. However, this takes a little more work to get a computer to display those colors properly.

The sketch below shoes a function `getRGB()` that takes a wavelength, in nanometers, and converts it to a RGB value, which can then be interpreted by p5. (Based on the work presented [here](http://www.efg2.com/Lab/ScienceAndEngineering/Spectra.htm))

{% include code-sketch-view.html whichSketch="colors.8" %}

This can be useful for creating sims about the spectrum of visible light, or lasers, or anything involving the physics of electromagnetic radiation in the visible region.

## Summary

It wouldn't be fair to say this article even scratches the surface of [color theory](https://en.wikipedia.org/wiki/Color_theory). How we perceive and describe colors is a fascinatingly huge topic about which much has been written. The poet/natural philosopher Goethe has a great book on the topic: [The Theory of Colors](https://en.wikipedia.org/wiki/Theory_of_Colours). As does Newton, [Opticks, or, A Treatise of the Reflexions, Refractions, Inflexions and Colours of Light](https://archive.org/details/Optics_285). Modern treatments are more accurate with regard to the physics and biophysics of color perception. But, here we are just concerned with how to get p5.js to display the colors we want. So, our job is easy, and by and large done! Bye.
