---
title: A slider
refno: slidertext.4
width: 300
height: 300
---

<script>

function setup() {
  canvas = createCanvas(300, 300);
  aSlider = createSlider(0,100,50,1);
  aSlider.position(50,20)

  aTextBox = createInput('');
  aTextBox.position(50,40);
  aTextBox.size(50)

  button = createButton('submit');
  button.position(aTextBox.x + aTextBox.width+10, aTextBox.y);

}

function draw() {
  background(200);
  ellipse(width/2,height/2,aSlider.value())
}
</script>
