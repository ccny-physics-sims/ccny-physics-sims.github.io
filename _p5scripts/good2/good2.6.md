---
title: Let's use translate
refno: good2.6
width: 300
height: 200
---

<script>

function setup() {
  canvas = createCanvas(300, 200);
  xSlider = createSlider(0,width,0,1)
  ySlider = createSlider(0,height,0,1)
  xSlider.position(10,10)
  ySlider.position(10,40)
}

function draw() {
  background(200);
  translate(xSlider.value(),ySlider.value())
  rect(0, 00, 50, 80);
}
</script>
