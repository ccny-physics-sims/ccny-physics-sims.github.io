---
title: A slider
refno: slidertext.1
width: 300
height: 300
---

<script>

function setup() {
  canvas = createCanvas(300, 300);
  aSlider = createSlider(0,100,50,1);
  aSlider.position(50,20)
}

function draw() {
  background(200);

}
</script>
