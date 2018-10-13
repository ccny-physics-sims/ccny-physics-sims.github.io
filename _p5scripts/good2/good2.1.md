---
title: A circle
refno: good2.1
width: 300
height: 200
---

<script>
var theta=0;

function setup() {
  canvas = createCanvas(300, 200);
}

function draw() {
  background(200);
  ellipse(width/2,height/2,100*sin(theta))
  theta+=0.01;
}
</script>
