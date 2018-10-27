---
layout: post
title: Sliders and Textboxes
date: 2018-10-25 9:00:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - intro
summary: Let's combine a slider and a text box to control a sketch
---

User interactions are one of the reasons p5 is such a great tool for building simple physics sims. Sliders can be used to adjust the value of somethings smoothly, while text boxes can be used to let users enter exact values. Sometimes we just want one or the other, other time we want both.

## 1. Making a slider

First, we'll make a slider. This is done by creating the slider, we will call it `aSlider`.

`aSlider = createSlider(0,100,50,1)`


The arguments in the parenthesis mean that the slider will range from 0 to 100, have an initial value of 50, and use increments of 1. We will position the slider at `x = 50` and `y=20` by adding the following line:

`aSlider.position(50,20)`

Run the sketch below to see the slider:

{% include code-sketch-view.html whichSketch="slidertext.1" %}

Next we want the slider to do something. Let's make it change the radius of a circle.

The line

`ellipse(width/2,height/2,slider.value())`

in the draw function creates and ellipse that located in the center with the third argument, its radius, being defined by the value of the slider: `aSlider.value()`.

{% include code-sketch-view.html whichSketch="slidertext.2" %}

## 2. Adding a textbox

We can create a textbox, called `aTextbox` by adding these two lines to the setup:

`aTextBox = createInput('');`

`aTextBox.position(50,40);`

{% include code-sketch-view.html whichSketch="slidertext.3" %}

## 3. Submit button

We also need a button to let the user tell the sketch to use the value from the textbox:

`button = createButton('submit');`

`button.position(textBox.x + textBox.width+10, textBox.y);`

{% include code-sketch-view.html whichSketch="slidertext.4" %}

One more thing for the button: it needs to do something. Let's make it trigger the function called `updateValue()`. Adding the line:

`button.mousePressed(updateValue);`

will take care of that. This is called a *method* in Javascript. The `.mousePressed(aFunction)` tells the button to execute the function contained in the `mousePressed()` argument when clicked.

{% include code-sketch-view.html whichSketch="slidertext.5" %}

## 4. Linking the slider and the textbox

Now we need the textbox value to set the slider, and visa-versa. We can use the following line to tell the slider to call a function (called `sliderChange`) every time it is changed. We do this by

`aSlider.input(sliderChange);`,

which is another use of the method construction. Now the method is the `input()` and it says to execute the `sliderChange()` function every time the slider value is changed.

And likewise, if the textbox is changed, the slider will adjust because we put

`aSlider.value(aTextBox.value())`

in the `updateValue()` function.

Run the sketch to see the linkage between all three things: the slider, the textbox, and the circle.

{% include code-sketch-view.html whichSketch="slidertext.6" %}

Ta-Da! Now both the slider and the textbox are linked and both can be used to control the circle's radius, or whatever parameter you want them too.
