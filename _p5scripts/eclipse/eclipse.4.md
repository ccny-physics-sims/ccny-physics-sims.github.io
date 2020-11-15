---
title: add a moon
refno: eclipse.4
width: 400
height: 400
---

<script>
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  translate(width/2,height/2)

  fill('yellow')
  circle(0,0,80)

  fill('white')
  circle(-40,0,80)
}</script>
