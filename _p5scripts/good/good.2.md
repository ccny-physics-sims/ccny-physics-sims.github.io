---
title: A slider and a circle
refno: good.2
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
  aSlider = createSlider(0,100,50,1)
  aSlider.position(10,10)
}

function draw() {
  background(200);
  radius = aSlider.value()
  ellipse(width/2,height/2,radius)
}
</script>
