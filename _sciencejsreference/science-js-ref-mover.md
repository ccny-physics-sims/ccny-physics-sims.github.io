---
title: Mover
subject: Reference
topics: Objects
summary: How to use the Science.js Mover object.
nice-name: science-js-ref-mover
contributors:
updated: 2017-04-05
layout: post
---

# Mover

The mover object makes a little ball that moves around.

#### Examples

##### Very simple moving ball

[a moving ball](http://ccny-physics-sims.github.io/science-library/examples/moving-ball/)

Just a regular ol' moving ball. It's red! And it bounces when it hits the wall.

##### Many moving balls

[a bunch of moving balls](http://ccny-physics-sims.github.io/science-library/examples/moving-balls/)

This example uses an array to create many moving balls, each with their own properties (e.g. velocity)

##### A ball and some vectors

[ball and vector](http://ccny-physics-sims.github.io/science-library/examples/moving-ball-vector/)

Here, we combine a mover and the arrow object to show the position and velocity vectors associated with a moving ball.

#### Mover properties

`Mover(position, velocity, acceleration, mass, color)`

`Mover.position` is a p5.Vector that gives this position of the mover

`Mover.velocity` is a p5.Vector that gives this velocity of the mover

`Mover.acceleration` is a p5.Vector that gives this acceleration of the mover

`Mover.limit` is a number that give the maximum velocity.

`Mover.mass` the movers can have mass.

`Mover.tail` the movers can leave little dots as they go. Boolean. Default is `false`.

`Mover.color` set the color of the ball using the p5 color specifications.