---
title: A slider moves an ever changing circle
refno: good2.5
width: 300
height: 200
---

<script>
var theta = 0;
function setup() {
  canvas = createCanvas(300, 200);
  aSlider = createSlider(-100,100,0,1)
  aSlider.position(10,10)
}

function draw() {
  background(200);
  yOffset = aSlider.value()
  ellipse(width/2,height/2-yOffset,50*sin(theta))
  theta+=.01
}
</script>
