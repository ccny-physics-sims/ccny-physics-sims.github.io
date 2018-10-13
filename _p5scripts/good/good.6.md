---
title: A slider
refno: good.6
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
  aSlider = createSlider(0,10,0,1);
  aSlider.position(20,20)
}

function draw() {
  clear()
  text('slider value is ' + aSlider.value().toFixed(2),100,100)
}</script>
