---
title: dynamic grays
refno: colors.2
width: 100
height: 100
---

<script>
function setup() {
  canvas = createCanvas(100, 100);
  }
function draw() {
  background(abs(255*sin(frameCount*.01)));
  fill(abs(255*cos(frameCount*.01)));
  text(abs((255*sin(frameCount*.01))).toFixed(0),width/2,height/2);
}
</script>
