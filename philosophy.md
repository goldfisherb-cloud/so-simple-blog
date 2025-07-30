---
layout: default
title: 哲思
permalink: /philosophy/
---

<h2>哲學文章 Philosophy</h2>
<ul>
  {% assign posts = site.categories.philosophy %}
  {% for post in posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
