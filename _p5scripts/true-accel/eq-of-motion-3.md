---
title: motion 3
refno: eq-of-motion.3
width: 600
height: 100
---

<script>
var x=0, dx;
function setup() {
  createCanvas(600,100);
  dx = 1;
}

function draw() {
  background(100);
  x += dx;
  ellipse(x,height/2,10,10);
}
</script>
