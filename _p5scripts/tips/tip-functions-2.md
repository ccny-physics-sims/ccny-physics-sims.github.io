---
title: Blank Canvas
refno: t.functions.2
width: 100
height: 100
---

<script>
function setup() {
  dr = 0;
}

function draw() {
  background(255);
  makeSomeShapes(dr);
  //dr increases by a little bit, each frame
  dr = dr + .05;
}

function makeSomeShapes(radiusChanger) {

  fill('blue');
  ellipse(50,50,20*sin(radiusChanger),20*sin(radiusChanger));
}
</script>
