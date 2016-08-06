---
layout: post
title:  Creating Your First Sketch With Codepen and P5.js
date:   2016-08-05 19:44:45 -0400
categories: coding
author: C. Newcomer
tags:
 - coding
 - sims
 - p5
 - intro
 - codepen
---

CodePen abstracts away most of the difficulties of setting up a development environment. This conveniently allows people without any web development background to start coding p5.js sketches right away.  

As there are already numerous tutorials available for learning p5.js, this will mostly focus on getting acquainted with using it on the CodePen platform. 


### Create a Pen

Make an account on [http://codepen.io/](CodePen). Then click "New Pen" to create your first Pen. 

!(codepen.png)

The HTML, CSS, and JavaScript files that make up a basic web page will be created for you automatically. You can simply write your code in the appropriate tab. Each panel is resizable. The display window, currently a blank white rectangle, shows a preview of your code's output. This display features live updating, which means it will automatically refresh any time you make changes to your work.

Note that if you want to keep your new Pen, you must click the save button in the upper right hand corner. Once you have done this, CodePen will automatically save your work every thirty seconds. 

### How to Use p5.js In CodePen

p5.js is what's known as a JavaScript library. A library is a collection of useful code snippets that you can include in your own program. For example, by including p5.js, we can draw a rectangle by writing "rect(0, 0, 20, 20)". This will draw a rectangle at (0,0) that is 20x20 in size. There's no need to manually specify how to draw a rectangle, because someone has already done it for us. We just have to tell the p5.js code snippet where we want our rectangle and how fat it should be, and it will handle the rest. 

In order to use a JavaScript library on CodePen, you will need to:

!(../post-imgs/codepen-intro/codepen2.png|767px)

1. Select the "Settings" tab in the top right corner of the page to bring up this menu. 

!(../post-imgs/codepen-intro/codepen3.png|767px)

2. Select the "JavaScript" option. 

!(../post-imgs/codepen-intro/codepen5.png|767px)

3. Look for the "Add External JavaScript" field. Libraries are often hosted on CDNs (Content Delivery Networks). Below I have provided two links to a CDN that hosts the libraries we need. 

> a.  https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.2/p5.min.js <--basic p5.js library

> b.  https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.2/addons/p5.dom.js <--p5.dom is an addon that will allow you to create sliders and buttons

**The order in which you list the libraries is important. The addon library p5.dom requires p5.js to run, so it should be listed after p5.js.**

!(../post-imgs/codepen-intro/codepen6.png|767px)

4. Select "Save & Close."

### Drawing an Ellipse in CodePen

Now that you have your Pen set up, let's try to draw something. Here is a p5.js code snippet that draws a circle on a grey background: 

<blockquote>
<pre>
var canvasWidth = 500;
var canvasHeight = 500;

function setup() {
  createCanvas(canvasWidth, canvasHeight);
  background('gray');
}

function draw() {
  // Draw a circle in the middle of the canvas
  ellipse(canvasWidth/2, canvasHeight/2, 100,100);
}
</pre>
</blockquote>

Copy this snippet into the tab that says "JavaScript." (Don't worry about the HTML and CSS tabs--they're ok on their own.) 

!(../post-imgs/codepen-intro/codepen8.png|767px)

Oh, we've got a sketch! But, it's kind of hard to see. We could scroll and squint, or resize the window panels, but it's easier to be lazy. 

!(../post-imgs/codepen-intro/codepen9.png|767px)

Click the "Change View" tab. 

!(../post-imgs/codepen-intro/codepen11.png|767px)

Here at the bottom we can select from multiple docking configurations for the code editor panels. Let's select the left one. 

!(../post-imgs/codepen-intro/codepen12.png|767px)

It's much easier to see this particular sketch, now! But, what if we want to preview it full screen? 

!(../post-imgs/codepen-intro/codepen14.png|767px)

Going back to our "Change View" mode, we see we have several other options. Select Debug Mode. 

!(../post-imgs/codepen-intro/codepen15.png|767px)

Now we can see our Pen as it will look in the browser. 

<b>As a free user, Debug Mode will only be visible to you. You will need to link others to Full Page mode (also available from the "Change View" menu).</b>

!(../post-imgs/codepen-intro/codepen16.png|767px)

This is our sketch as seen in Full Page Mode. It has a small CodePen banner but otherwise looks very similar to Debug Mode.

### Escaping From CodePen

Nice as CodePen is, we'll want to put our sketches up on our own site eventually. How can we rescue them? The export function!


!(../post-imgs/codepen-intro/codepen17.png|767px)

Look down at the bottom right corner. 

!(../post-imgs/codepen-intro/codepen18.png|767px)

Click "Export .zip." 

!(../post-imgs/codepen-intro/codepen19.png|767px)

Unzip the archive, then double-click "index.html." You should see your ellipse displayed in your browser. 

**Investigating these exported files should also give some insight into how a basic webpage is put together.**

### Troubleshooting Using Your Browser

Your browser contains something called a console. (If you've programmed before, this is the browser's equivalent of the command line or terminal.) Errors and warnings that occur on a web page will be logged here, but it's hidden by default. Windows users can view it on Chrome by pressing Ctrl-Shift-J, or  Ctrl-Shift-I on Firefox. For Mac users, see [https://www.wickedlysmart.com/hfjsconsole/ this]. For anything else, google "keyboard shortcut for [your browser here] console [your operating system]."

!(../post-imgs/codepen-intro/codepen20.png|767px)

Say we are very bad at typing and accidentally mangled the spelling of "ellipse." 

!(../post-imgs/codepen-intro/codepen21.jpg|767px)

The console will usually give us some idea of what is happening. If you click the triangle to the left of "Uncaught ReferenceError," it will expand to reveal even more information. Googling various bits of information from here will usually help figure out where you've gone astray. In this case, we don't need to google--"elipse is not defined" should call attention to the fact that we've drastically misspelled it.

<b>You may have noticed there's a "Console" setting on the lower left side of the CodePen window. This is a simulated console and it is extremely buggy. Avoid using it. The real console is much more trustworthy and just as easy to use. </b>

### Troubleshooting Using CodePen

CodePen's text editor has a built in error detector. It won't catch everything, but it'll catch some things. 

!(../post-imgs/codepen-intro/codepen22.png|767px)

Sometimes a red circle or triangle will appear. Click it and it will give you a hint as to what went wrong. 

!(../post-imgs/codepen-intro/codepen23.png|767px)

Sometimes this can be rather vague. In this case, the trouble is that ellipse takes four inputs, but has only been provided with one. The input ended unexpectedly early because it was not given the other three.

### Tidying Using CodePen

CodePen will do its best to indent your code for you as you go, but sometimes a little manual repair is needed.

!(../post-imgs/codepen-intro/codepen24.png|767px)

Assume we had a late night coding session, and our code now looks a bit messy in the harshness of the morning light.

!(../post-imgs/codepen-intro/codepen25.png|767px)

Click the top right menu arrow, and select "Tidy JS" from the dropdown menu.

!(../post-imgs/codepen-intro/codepen26.png|767px)

Ta-da!

### Summary

CodePen's excellent for quickly prototyping small projects or trying out new techniques. It also makes it really easy to send something to a friend or coworker--it's already online, so all you have to do is send them the link!

