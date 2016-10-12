---
title: motion 10
refno: eq-of-motion.10
width: 500
height: 500
---

<script>
var previousVel;
function setup() {
  createCanvas(500,500);
  currentVel = 0;
  accel = 11;
  frameRate(2);
  y = 10;
  x = 10;
}

function draw() {
  fill('blue');
  ellipse(x,y,10,10);
  previousVel = currentVel;
  currentVel += accel;
  averageVel = (previousVel + currentVel)/2;
  y += averageVel;
  x += 30;
  drawParabola()
  if (x>500){noLoop()}
}
function drawParabola(){
noFill();
stroke(0);
translate(10,10);
beginShape();
curveVertex(0,0);
for (i=0;i<20;i++){
  curveVertex(i*30, .5*11*Math.pow(i,2))
}
endShape();
}
</script>
