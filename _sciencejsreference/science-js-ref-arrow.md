---
title: Arrow
subject: Reference
topics: Objects
summary: How to use the Science.js Arrow object.
nice-name: science-js-ref-arrow
contributors:
updated: 2017-04-05
layout: post
---

# Arrow

The arrow gives a nice triangular tipped arrow useful for showing the direction and magnitude of a vector.

To declare an arrow use the following:
```javascript
var my_arrow = new Arrow(origin_,target_);

/*where both of the parameters are P5.js vector objects*/
```

#### Usage

The following will create the object.
```
aVector = new Arrow(startPoint, endPoint);
```
To display it:
```
aVector.update();
aVector.display();
```


The statement asks for: `Arrow(origin_, target_)`

`origin_` and `target_` are [p5.Vector](http://p5js.org/reference/#/p5.Vector) objects

#### arrow properties:

`Arrow.color` sets the color of the arrow. (the defualt color is white)

for example:

`Arrow.color = color(20,20,230);` will give you a nice blue vector. Or, you could just write `Arrow.color = color('blue')` and p5 will make translate that to RGB values.

`Arrow.width` give the thickness of the arrow shaft. Default is 20px.

`Arrow.showComponents` is a boolean that indicates whether the x/y components should be shown. Default is `false`.

`Arrow.draggable` is a boolean that indicates whether the arrow should be draggable by the user or not. Default is `true`.

`Arrow.grab` is a boolean that indicates whether the user can grab the tip and change the direction/magnitude of the arrow. Default is `true`.

#### Examples:

##### A simple Vector
[simple-vector](http://ccny-physics-sims.github.io/science-library/examples/simple-vector/)

This example shows a vector that can be dragged and grabbed. (i.e. translated and modified in dir/magnitude)

##### A rotating Vector
[rotating-vector](http://ccny-physics-sims.github.io/science-library/examples/rotating-vector/)

Here's a vector that rotates at some speed.

##### Another rotating Vector
[rotating-vector-2](http://ccny-physics-sims.github.io/science-library/examples/rotating-vector-2/)

Here's a vector that rotates at some speed, and always points towards the center.

##### Vector Addition
[Vector Addition ](http://ccny-physics-sims.github.io/science-library/examples/vector-addition/)

This example shows the sum of two vectors graphically.

##### Random Walks
[Random Walks](http://ccny-physics-sims.github.io/science-library/examples/random-walk/)

Add up 10 random displacements and what do you get? A random walk.