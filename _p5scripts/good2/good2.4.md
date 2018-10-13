---
title: A slider moves circle
refno: good2.4
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
  aSlider = createSlider(-100,100,0,1)
  aSlider.position(10,10)
}

function draw() {
  background(200);
  yOffset = aSlider.value()
  ellipse(width/2,height/2-yOffset,20)
}
</script>
