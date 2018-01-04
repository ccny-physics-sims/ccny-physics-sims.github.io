---
layout: page
title: Learning
permalink: /learning/
navigation_weight: 1
order: 4
excerpt: learn to build a physics sim
---

## Some quick tips:

{% for tip in site.quick-tips %}
  - [{{tip.title}}]({{site.baseurl}}{{tip.url}})
{% endfor %}

## Longer Tutorials:

{% for tutorial in site.tutorials %}
  - [{{tutorial.title}}]({{site.baseurl}}{{tutorial.url}}):
{{tutorial.summary}}

{% endfor %}
