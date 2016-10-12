---
title: motion 5
refno: eq-of-motion.5
width: 600
height: 100
---

<script>
var x=0, vel, accel;
function setup() {
  createCanvas(600,100);
  vel = 0;
  accel = 0.05;
}

function draw() {
  background(100);
  x += vel;
  vel += accel;
  ellipse(x,height/2,10,10);
}
</script>
