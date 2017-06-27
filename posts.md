---
layout: page
title: Posts
permalink: /posts/
navigation_weight: 1
order: 3
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <p>
        {{ post.date | date: "%b %-d, %Y" }} --- {{ post.content | strip_html | truncatewords: 50 }}
      </p>
    </li>
  {% endfor %}
</ul>
