---
layout: post
title:  test codes
date:   2016-07-05 19:44:45 -0400
categories: coding
---



{% assign codetoshow = site.collections.p5scripts | where: 'id', 'simple-ellipse' %}





 {{site.p5scripts | where: "refno", "1.1"}} 


```
{{site.p5scripts | where: "refno", "1.1"}}
```

{% assign toshow = site.p5scripts | where: "refno", "1.1" %}

 <iframe src="{{baseurl}}{{toshow[0].url}}.html"></iframe>

<!-- <iframe src="{{baseurl}}{{codetoshow[0].url}}.html"></iframe> -->


<!--
<iframe src="{{baseurl}}{{codetoshow[0].url}}.html"></iframe>



{% assign codetoshow = site.p5scripts | where: 'name', move-ellipse-fill %}
```
{{codetoshow[1]}}
```
<iframe src="{{baseurl}}{{codetoshow[1].url}}.html"></iframe> -->
