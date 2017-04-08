---
title: Free Body Diagram
subject: Reference
topics: Objects
summary: How to use the Science.js Moving FBD object.
nice-name: science-js-ref-fbd
contributors:
updated: 2017-04-05
layout: post
---

# Free body diagrams

*Note: this feature is still under major development*

Here's a simple example

[free body diagram](http://ccny-physics-sims.github.io/science-library/examples/free-body-diagram/)

`a_free_body_diagram = new FBD(position_, howManyForces_,showResultant_);`


Define the forces using arrays:

```
a_free_body_diagram.mag = [force1mag,force2mag,force3mag];
a_free_body_diagram.direction = [force1direction,force2direction,force2direction]
a_free_body_diagram.xoffsets = [0,0,0]
a_free_body_diagram.yoffsets = [0,0,0]
a_free_body_diagram.labels = ['force 1','force 2','force 3']
```

The offsets can be used for clarity if you have two or more forces on an object pointing in the same direction.

Update and display the fbd using:

```
a_free_body_diagram.update();
a_free_body_diagram.display();
```
