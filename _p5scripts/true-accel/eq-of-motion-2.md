---
title: motion 2
refno: eq-of-motion.2
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
  fill(120);
  rect(width/2,0,width/2,height);
  t+=1;
  //let's change the acceleration based on position
  if (x>width/2) {a=0;}
  //equation of motion
  x = x0 + v0*t + 0.5* a * Math.pow(t,2);
  fill(250);
  ellipse(x,height/2,10,10)

}
</script>
