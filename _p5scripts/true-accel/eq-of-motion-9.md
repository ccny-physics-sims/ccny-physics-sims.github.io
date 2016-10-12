---
title: motion 9
refno: eq-of-motion.9
width: 600
height: 100
---

<script>
var x0=0, x1=0, v0=0, t=0, vel, accel, previousVel, currentVel;
function setup() {
  createCanvas(600,100);
  vel = 0;
  currentVel = 0;
  accel = 11;
  frameRate(2);
}

function draw() {
  //method 1
  x = x0 + v0*t + 0.5* accel * Math.pow(t,2);
  t+=1;
  fill('green');
  ellipse(x,height/2.5,10,10);
  //method 3
  fill('blue');
  ellipse(x1,height/1.5,10,10);
  previousVel = currentVel;
  currentVel += accel;
  averageVel = (previousVel + currentVel)/2;
  x1 += averageVel;
}
</script>
