---
layout: post
title: Files and Folders
date: 2016-07-23 9:40:45 -0400
categories: coding
author: J. Hedberg
tags:
 - coding
 - sims
 - p5
 - intro
---

When it comes time to putting a sim on the web, for all to see and use, it has to follow some structural guidelines. There will be two files needed: a) `sketch.js` and b) `index.html`. They will both be in the same folder.


### sketch.js

Let's look at each file, starting with the first: `sketch.js`.

This is our p5 sketch, duh. It usually looks something like this:

```javascript
function setup(){
  canvas = createCanvas(400,600)  
}

function draw(){
  //make cool things
  translate(width*0.5, height*0.5);
  rotate(frameCount / 50.0);
  star(0, 0, 80, 100, 40);
}
```

But how do we get our browser to do these cool things? For that, we need the seconds file, the `index.html`

### index.html

The `index.html` file is the web page that we use the browser to open. In that page are instructions for the browser. Here's a very basic `index.html` file:

```html
<!DOCTYPE html>
<html>

<head>
<!-- meta stuff -->
</head>

<body>
<!-- page content -->
</body>

</html>

```

This one does nothing. But it shows the basic structure:

* A `DOCTYPE` command is the first line. This tells the browser how to interpret the file.
* The next _tag_ is the `<html>` tag. It says that everything after (and before the closing `</html>` tag) is html instructions.
* Next comes the `<head>`. In there we'll put stuff like a title tag, and links to style instructions, and other things that aren't part of the main page you will see. That all goes in the `<body>` tag.
* Now, we're at the `<body`> tag. In here goes the content of the webpage. For example, you could put a paragraph about the history of peanut butter:

```html
<body>
<!-- page content -->
<p>
Though peanut butter has origins in the days of the ancient Incas and Aztecs, it wasn't patented until 1884 by Marcellus Edson in Montreal, Quebec.
</p>
</body>
```

* Each tag is then _closed_ as the page progresses. _Closing_ a tag just means to tell the browser we're done with the body, or a paragraph.

```html
<!-- start tag! -->
<body>
Stuff
<!-- close the body -->
</body>
```

### Thing in the Head

So, back to our index page. Let's add a few things to the *head*. First, we want a title our page:

```html
<title>Simulating Nature</title>
```

That will go in the head.

Also, we need to get the p5.js library. We'll get it from the internet, but allow for the possibility that we might not be connected, so let's also have a version saved on our computer we can use. The two lines enclosed in the `<script>` tag do these two things. The first try to get it from a *content delivery network*, (or CDN). If that fails for some reason, we can get it from a locally stored version.

```html
<!-- get p5.js from CDN -->
<script language="javascript" src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.2/p5.min.js"></script>
<!-- uh oh. Can't find CDN?, then load from local. -->
<script>
window.p5 || document.write('<script src="../../../js/p5.js"><\/script><script src="../../../js/addons/p5.dom.min.js"><\/script>');
</script>
```

Next we need to get our `sketch.js` file. That's where our p5 that we've written will live.

```html
<script language="javascript" src="sketch.js"></script>
```

If it's in the same folder as the `index.html` page, then we don't have to do any directory shuffling to access it.

So, all together, our `index.html` file now looks like this:

```html
<!DOCTYPE html>
<html>
<head>
<title>Simulating Nature</title>
<!-- get p5.js from CDN -->
<script language="javascript" src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.2/p5.min.js"></script>
<!-- uh oh. Can't find CDN?, then load from local. -->
<script>
window.p5 || document.write('<script src="../../../js/p5.js"><\/script><script src="../../../js/addons/p5.dom.min.js"><\/script>');
</script>

<script language="javascript" src="sketch.js"></script>

</head>

<body>
</body>

</html>

```

So, now our directory might structure might look like

```
Folder: a-sim/
--> index.html
--> sketch.js
```

When we navigate to the url `www.whatever.com/a-sim/` the browser will load the `index.html` page, which in turn loads the necessary javascript files. We should see our awesome sim!
