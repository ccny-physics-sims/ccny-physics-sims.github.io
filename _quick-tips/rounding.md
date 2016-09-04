---
title: Rounding
---

## About numbers and rounding

Sometimes we want to display numbers as part of a sim. If you have a variable, like `velocityOfCat` for example, and want to display it using the function `text(velocityOfCat)` you might end up seeing a number with a lot of decimal places after it, (press play below to see a demo)

<script type="text/p5" data-preview-width="400">
function setup() {
  createCanvas(200, 100);
}

function draw() {
  background(240, 240, 240);
  velocityOfCat = Math.sqrt(frameCount);
  fill('black')
  text("velocity of cat: " + velocityOfCat,10,10);
}
</script>

That many decimal places is obviously not too useful. So, we can use the function `toFixed()` to trim those unsightly numbers:

<script type="text/p5" data-preview-width="400">
function setup() {
  createCanvas(200, 100);
}

function draw() {
  background(240, 240, 240);
  velocityOfCat = Math.sqrt(frameCount);
  fill('black')
  text("velocity of cat: " + velocityOfCat.toFixed(2),10,10);

}
</script>

Other methods also exists for this. You can use the rounding functions of Javascript as well:

```
Math.round(velocityOfDog * 100) / 100 ;
```

will output something with 2 decimal places. 
