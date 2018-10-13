---
title: One circle, all over the place.
refno: good.3
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
}

function draw() {
  background('blue');
  fill('orange');
  ellipse(random(width),random(height),30);
}</script>
