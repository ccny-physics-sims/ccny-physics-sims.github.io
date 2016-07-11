---
title: About functions
---

## About functions

A function, in our context, is essentially a way of references a set of instructions, without having to write them all out again.

An analogy: Someone says "clean your room", that means do a whole bunch of other things (i.e. pick up cloths off floor; change bed sheets; remove old coffee cups). `CleanYourRoom()` is interpreted by you to mean _do all those things_.

```javascript
function CleanYourRoom() {
    pick up clothes
    change bed sheets
    remove old coffee cups
}
```


So, we can write functions (i.e. a list of commands) for the program to execute without having to write out each command over and over.

To create a function in javascript, all you need you to do is add some parenthesis after the name, then enclose the instructions with curly brackets.

```javascript
function myFunction() {
  instructions
}
```

Here's a simple function, called `makeSomeShapes()` written in a p5 sketch that makes a few shapes.

{% include code-sketch-view.html whichSketch="t.functions.1" %}

We can also _pass the function an argument_, by enclosing a variable inside the parenthesis part. In this example, I'll pass the `makeSomeShapes()` function a variable called `dr`. We'll use this to change the diameter of the ellipse every frame. You'll note in the definition of the function, I called it `radiusChanger`

{% include code-sketch-view.html whichSketch="t.functions.2" %}

You can pass a function several _arguments_. Just separate them by commas:

```javascript
function makeJuice(whichKind, howMuch, temperature){
 // juice making instructions
}
```

### More

Here is a nice, thorough discussion of functions:

[javascript functions](http://eloquentjavascript.net/03_functions.html)
