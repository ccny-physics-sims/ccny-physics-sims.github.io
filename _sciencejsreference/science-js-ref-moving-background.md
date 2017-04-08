---
title: Moving Background
subject: Reference
topics: Objects
summary: How to use the Science.js Moving Background object.
nice-name: science-js-ref-moving-background-usage
contributors:
updated: 2017-04-05
layout: post
---

# Moving Background

Let's say you want to convey motion, without making an object move? Then use the moving-background object.

#### Examples

##### Linear Motion
[linear motion](http://ccny-physics-sims.github.io/science-library/examples/moving-background-cityStreet/)

A simple 1-d motion system. The object stays still, but motion is understood via the background.

##### 2d Motion
[2d motion](http://ccny-physics-sims.github.io/science-library/examples/moving-background-clouds/)

A 2d system. The green vector shows velocity; the purple vector shows acceleration.

#### Moving background properties

`movingBackground(whichKind,basePosition,velocity,acceleration);`

`whichKind` determines what the background is. Right now, there are two options: `'cityStreet'` or `'clouds'`. `cityStreet` is good for linear motion in x. `clouds` is more appropriate for an object moving in x and y.

`basePosition` is a p5.Vector that gives the center location of the backgroun.

`velocity` is a p5.Vector that indicates the initial velocity of the background.

`acceleration` is a p5.Vector that indicates the acceleration of the background, i.e. how the velocity changes. This of course, could change.

```
bg.update()
bg.display();
```

will update and draw the background