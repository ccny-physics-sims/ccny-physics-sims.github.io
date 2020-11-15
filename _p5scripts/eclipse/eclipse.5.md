---
title: move the moon
refno: eclipse.5
width: 400
height: 400
---

<script>
function setup() {
  createCanvas(400, 400);
  slider = createSlider(-80, 80, -80);
  slider.position(10, 10);
}

function draw() {
  background(220);
  translate(width/2,height/2)

  val = slider.value();

  fill('yellow')
  circle(0,0,80)

  fill('white')
  circle(val,0,80)
}</script>
