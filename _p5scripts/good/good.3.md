---
title: A slider and a circle
refno: good.3
width: 300
height: 200
---

<script>
var theta = 0;
function setup() {
  canvas = createCanvas(300, 200);  
}

function draw() {
  background(200);
  radius = 20
  ellipse(width/2,height/2+30*sin(theta),radius)
  theta+=.1;
}
</script>
