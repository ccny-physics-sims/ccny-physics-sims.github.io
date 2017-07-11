---
layout: post
title:  A vintage simulation, redone.
date: 2016-08-10 16:23:00 -0400
categories: physics
author: J. Hedberg
---



In the late 1960's, Frank Sinden, a mathematician at Bell Labs, created one of the earliest computer animations. It featured some basic examples of elementary physics: how a mass will respond to a force, the effects of the familiar inverse square law of Newtonian gravitation on particles, and even non-physical examples such as a force proportional to the cube of the distance between two objects. Each concept is accompanied by a strikingly simple, yet powerful animation. Here's the video below. (you might need to allow 'unsafe scripts' to watch it. Or visit: <a href="http://techchannel.att.com/play-video.cfm/2012/8/20/AT&T-Archives-Force-Mass-Motion">here</a>)

<iframe width="560" height="315" src="http://techchannel.att.com/embed/index.cfm?mediaID=11125&w=560&h=315" frameborder="0" allowfullscreen ></iframe>

The computers required to construct these visualizations where no doubt much larger than a modern desktop. And, each frame of the animation had to be printed individually and developed in a darkroom attached to the mainframe. All these difficulties aside, the animation does a fantastic job illustrating the essential character of Newton's second law: That the change in velocity of an object is proportional to the force applied, and inversely proportional to its mass, or F = ma.

So, to honor this valiant work (imagine developing _each frame_ ), I've built a replica of part of Sinden's animation using the [p5.js](http://www.p5js.org) javascript library. Click within the black frame below and then use the arrow keys to add force to the moving mass. One vector indicates the velocity of the mass, the other, its acceleration.

<iframe src="https://ccny-physics-sims.github.io/sims/force-motion/" width ="500" height="500" ></iframe >

For a better experience, or if you're on a mobile device, click here to launch a full screen version. (Tilting on mobile increases or decreases the acceleration of the mass)

[Force-Motion c. 2016](https://ccny-physics-sims.github.io/sims/force-motion/)

Want to look under the hood? Here is the [source code](https://github.com/ccny-physics-sims/sims/blob/gh-pages/force-motion/sketch.js).



And, be sure to check out some of our newer, modern [science sims]({{site.url}}/sims-catalog) while you're here!

References:

[http://techchannel.att.com/play-video.cfm/2012/8/20/AT&T-Archives-Force-Mass-Motion](http://techchannel.att.com/play-video.cfm/2012/8/20/AT&T-Archives-Force-Mass-Motion)
