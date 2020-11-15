---
title: More bells and whistles
refno: eclipse.6
width: 400
height: 400
---

<script>
let slider;
let val;
function setup() {
  createCanvas(400, 400);
  slider = createSlider(-80, 80, -80);
  slider.position(10, 10);
  slider.style('width', '100px');
  slider.style('border-radius', '50%');
  colorMode(HSB)
}

function draw() {
  val = slider.value();

  background(color(204,30,map(abs(val),0,80,10,80)));
  translate(width/2,height/2)
  makeStars(500)
  // stroke('yellow')
  fill('yellow')
  circle(0,0,80)
  fill(color(204,30,map(abs(val),0,80,10,80)))
  stroke(color(204,30,map(abs(val),0,80,50,90),.3))
  circle(val,0,80)

}
function makeStars(howMany) {
  randomSeed(99);
  noStroke()
  fill(color(204,30,map(abs(val),0,80,75,80)))
  for (i=0;i<howMany;i++)
  {
    circle(random(-windowWidth,windowWidth), random(-windowHeight, windowHeight),random(1,5))  
  }

       }</script>
