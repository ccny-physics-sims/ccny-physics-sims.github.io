---
title: Blank Canvas
refno: t.functions.1
width: 100
height: 100
---

<script>
function setup() {
}

function draw() {
  //call our function
  makeSomeShapes();
}

function makeSomeShapes() {
  fill('red');
  ellipse(50,50,20,20);
  fill('blue');
  ellipse(20,10,10,10);
}
</script>
