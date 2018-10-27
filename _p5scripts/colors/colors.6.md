---
title: Hue wheel
refno: colors.6
width: 300
height: 300
---

<script>
function setup() {
  canvas = createCanvas(300, 300);
  background(255);
  translate(width/2,height/2)
  for (i = 0; i<360; i++){
    c = color('hsl('+i+', 100%, 50%)');
    stroke(c)
    rotate(radians(1));
    line(30,0,70,0);
  }
}

</script>
