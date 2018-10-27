---
title: A slider
refno: slidertext.5
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
  button.mousePressed(updateValue);

  background(200);

}

function draw() {
  ellipse(width/2,height/2,aSlider.value())
}

function updateValue(){
  background('red');
}
</script>
