---
title: A slider
refno: slidertext.6
width: 300
height: 300
---

<script>

function setup() {
  canvas = createCanvas(300, 300);
  aSlider = createSlider(0,100,50,1);
  aSlider.position(50,20)
  aSlider.input(sliderChange);

  aTextBox = createInput('');
  aTextBox.position(50,40);
  aTextBox.size(50)
  aTextBox.value(aSlider.value());

  button = createButton('submit');
  button.position(aTextBox.x + aTextBox.width+10, aTextBox.y);
  button.mousePressed(updateValue);


}

function draw() {
  background(200);
  ellipse(width/2,height/2,aSlider.value())
}

function updateValue(){
  aSlider.value(aTextBox.value())
}

function sliderChange() {
  aTextBox.value(aSlider.value());
}
</script>
