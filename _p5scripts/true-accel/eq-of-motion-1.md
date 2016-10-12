---
title: motion 1
refno: eq-of-motion.1
width: 600
height: 100
---

<script>
var x=0, x0=0, v0=0, a=.05, t=0;
function setup() {
  createCanvas(600,100);
}

function draw() {
  background(100);
  t+=1;
  //equation of motion
  x = x0 + v0*t + 0.5* a * Math.pow(t,2);
  ellipse(x,height/2,10,10)
}
</script>
