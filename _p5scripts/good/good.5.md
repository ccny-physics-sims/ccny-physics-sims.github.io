---
title: Mathy
refno: good.5
width: 300
height: 200
---

<script>
function setup() {
  canvas = createCanvas(300, 200);
}

function draw() {
  clear()
  line(0,0,mouseX,mouseY)
  text((atan2(mouseY,mouseX)*180/PI).toFixed(2)+' degrees',150,100)
}</script>
