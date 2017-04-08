---
title: embedding from script
subject: Reference
topics: Testing
summary: HTF do I embed codes
nice-name: science-js-test
contributors:
updated: 2017-04-05
layout: post
custom-css: github-embed
custom-js: github-embed-min
---



<body>
  <h2>Test Embed</h2>
  


    <div id="embedded-code"></div>
	
	
	

<script>
 githubEmbed('#embedded-code', {
    	"owner": "ccny-physics-sims",
        "repo": "science-library",
        "ref": "master/examples/rotating-wheel",
 
    	"embed": [{
    		"path": "sketch.js",
          "label": "thisisafile.js",
    	}]
    });
</script>
</body>