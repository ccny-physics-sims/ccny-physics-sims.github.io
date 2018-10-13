---
title: A lot of circles
refno: good.2
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
  background('blue');

}

function draw() {
  fill('orange');
  ellipse(random(width),random(height),30);
}</script>
