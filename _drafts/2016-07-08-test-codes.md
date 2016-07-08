---
layout: post
title:  test codes
date:   2016-07-05 19:44:45 -0400
categories: coding
---



{% assign codetoshow = site.collections.tutorials | where: 'id', 'simple-ellipse' %}





 {{site.tutorials | where: "refno", "1.1"}} 


```
{{site.tutorials | where: "refno", "1.1"}}
```

{% assign toshow = site.tutorials | where: "refno", "1.1" %}

 <iframe src="{{baseurl}}{{toshow[0].url}}.html"></iframe>

<!-- <iframe src="{{baseurl}}{{codetoshow[0].url}}.html"></iframe> -->


<!--
<iframe src="{{baseurl}}{{codetoshow[0].url}}.html"></iframe>



{% assign codetoshow = site.tutorials | where: 'name', move-ellipse-fill %}
```
{{codetoshow[1]}}
```
<iframe src="{{baseurl}}{{codetoshow[1].url}}.html"></iframe> -->
