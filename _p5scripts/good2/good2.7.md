---
title: Let's use translate and rotate
refno: good2.7
width: 300
height: 200
---

<script>
var theta = 0;
function setup() {
  canvas = createCanvas(300, 200);
  rectMode(RADIUS)
}

function draw() {
  background(200);
  translate(width/2,height/2)
  rotate(theta)
  rect(0, 0, 10, 15);
  theta+=.01;
}
</script>
