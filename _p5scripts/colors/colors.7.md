---
title: HSL part 2
refno: colors.7
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
  background(255);
  strokeWeight(4)
  for (i = 0; i<width; i+=10){
    c = color('hsl(200,100%,'+map(i,0,width,0,100)+'%)');
    stroke(c)
    line(i,0,i,height/2);
    c = color('hsl(200,'+map(i,0,width,0,100)+'%,50%)');
    stroke(c)
    line(i,height/2,i,height);
  }
}</script>
