---
title: motion 4
refno: eq-of-motion.4
width: 600
height: 100
---

<script>
var x=0, vel;
function setup() {
  createCanvas(600,100);
  vel = 1;
}

function draw() {
  background(100);
  fill(120);
  rect(width/2,0,width/2,height);
  //if the particle goes past halfway, make the velocity 3 times faster.
  if (x>width/2){vel=3};
  x += vel;
  fill(255);
  ellipse(x,height/2,10,10);
}
</script>
