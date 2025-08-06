---
layout: default
title: 生活
permalink: /life/
---

<h2>生活相關 Life</h2>
<ul>
  {% assign posts = site.categories.life %}
  {% for post in posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
