---
title: for
refno: good2.9
width: 300
height: 200
---

<script>
var balls = []
function setup() {
  canvas = createCanvas(300, 200);
  for (var i=0; i<50; i++) {
    balls.push(new makeABall());
  }
}

function draw() {
  background(200);
  translate(width/2,height/2)
  for (var i=0; i<balls.length; i++) {
    balls[i].update();
    balls[i].display();
  }
}

function makeABall(){
  this.theta = random(0,360);
  this.r = random(30,50);
  this.diameter = random(10, 30);
  this.update = function() {
    this.theta+=.01
  };
  this.display = function() {
    ellipse(this.r*cos(this.theta), this.r*sin(this.theta), this.diameter);
  };
}
</script>
