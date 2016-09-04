---
layout: post
title: Styling your sim
date: 2016-09-04 08:32:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - intro
summary: Want to spruce up your sim? Use our style sheet to make it pretty.
---

When we use certain elements in a sim, like a slider or a button, we have the option of styling it. This means, we can select a color, shape, even behavior (eg should it change color when your mouse hovers over it?). To unify the our science sims, we now have a stylesheet that can be applied to all these element so that our buttons and sliders looks and act the same across all the sims. This makes them easier to use by reducing the overhead associated with varying designs.

To begin using the style sheet, we first need to get it! That can be done by adding the following line to the `<head>` section of your `index.html` file. (Make sure to read the tutorial [files and folders](files-and-folders) if you're not happy with this sentence!)

```html
<link href="https://ccny-physics-sims.github.io/sim-design/sims-styles.css" rel="stylesheet" />
```

or if you're ready for deployment, you can reference it using the relative url:

```html
<link href="../../sim-design/sims-styles.css" rel="stylesheet" />
```

assuming your directories match the github repos structure.

Once you have properly referenced the stylesheet, you can begin to use the styles. You can see all the various elements in an example file here:

[https://ccny-physics-sims.github.io/sim-design/index.html](https://ccny-physics-sims.github.io/sim-design/index.html)

<iframe src="https://ccny-physics-sims.github.io/sim-design/index.html" width="800" height="500" ></iframe>

### Buttons

So, we can start with a button:

To make a button in p5, you need to use the [DOM library](http://p5js.org/reference/#/libraries/p5.dom) and then create a button using `createButton()`. [[ref]](http://p5js.org/reference/#/p5/createButton).

Here's a sim that uses a button to start and stop an animation:

<iframe src="https://ccny-physics-sims.github.io/sims/pendulum-plots/" width ="800" height="460" ></iframe >

The lines of code responsible for making the button are here:

```js
onoff = createButton("start");
onoff.mouseClicked(turnonoff);
onoff.position(50,300);
onoff.class("sim-button gray");
```

Line 1 creates the "start" button and assigns it the variable name `onoff`. The next line tells the program what to do when you click the button (i.e. run the function `turnonoff()`. The 3rd line give the position of the button. And the forth line add a **class** to the button. The class is what will give it its style. Here, we've added two classes: `sim-button` and `gray`. By giving it these classes, we have effectively told it to follow all the instructions in the css file describing what a `sim-button` should look like. If you look at the code for the css file, you can find them around line 222.

```css
.sim-button {
  width:100px;
  padding: 15px 25px;
  font-size: 15px;
  font-family:Helvetica, sans-serif;
  font-weight:bold;
  cursor: pointer;
  text-align: center;
  outline: none;
  color: #fff;
  background-color: #94c6d8;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}
```

The default button is blue, but we want this one to be gray, so we add another class `gray` to the button. Voila! We now have a nice gray button.

### Sliders

Sliders are slider more complicated input devices, but the css model allows us to style them the same way - just add the class `sim-slider` to a slider object and you get a nice pretty slider.

Here's a sim with some sliders:

<iframe src="https://ccny-physics-sims.github.io/sims/parabola-plot/" width ="700" height="500" ></iframe >

This code creates a slider:

```js
aSlider = createSlider(-20, 20, 1);
aSlider.position(50,120);
aSlider.class("sim-slider");
```

Again, all we need to do is add the class 'sim-slider'.

There are also radio boxes, and checkboxes. Again, all you need to do is add the class. You can read more about this in the documentation found here:

[https://github.com/ccny-physics-sims/sim-design](https://github.com/ccny-physics-sims/sim-design)
