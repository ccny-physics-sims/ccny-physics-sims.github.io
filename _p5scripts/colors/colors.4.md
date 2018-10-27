---
title: dynamic color change
refno: colors.4
width: 200
height: 100
---

<script>
function setup() {
  canvas = createCanvas(200, 100);
  aSlider = createSlider(0,255,255,1)
  aSlider.position(50,height/2)
  }
function draw() {
  c = color(aSlider.value(),50,50)
  background(c);
}
</script>
