---
title: motion 8
refno: eq-of-motion.8
width: 600
height: 100
---

<script>
var x1=0, vel, accel, previousVel;
function setup() {
  createCanvas(600,100);
  currentVel = 0;
  accel = .2;
}

function draw() {
  background(100);
  previousVel = currentVel;
  currentVel += accel;
  averageVel = (previousVel + currentVel)/2;
  x1 += averageVel;
  ellipse(x1,height/2.5,10,10);
}
</script>
