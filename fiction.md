---
layout: default
title: 創作
permalink: /fiction/
---

<h2>小說創作 Fiction</h2>
<ul>
  {% assign posts = site.categories.fiction %}
  {% for post in posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
