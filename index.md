
---
layout: default
title: Home
---

<h2>哲思 Philosophy</h2>
<ul>
  {% for post in site.categories.philosophy %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>

<h2>科普 Science</h2>
<ul>
  {% for post in site.categories.science %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>

<h2>創作 Fiction</h2>
<ul>
  {% for post in site.categories.fiction %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>

<h2>生活 Life</h2>
<ul>
  {% for post in site.categories.life %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
