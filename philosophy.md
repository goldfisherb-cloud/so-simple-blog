---
layout: default
title: 哲思
permalink: /philosophy/
---

<h2>哲思文章 Thinking</h2>

<div class="entries-list">
  {% assign posts = site.categories.philosophy %}
  {% for post in posts %}
    <article class="entry">
      {% if post.image %}
        <header class="entry-header">
          <div class="entry-image">
            <img src="{{ post.image }}" alt="{{ post.title }}">
          </div>
        </header>
      {% endif %}
      
      <div class="entry-content">
        <h3 class="entry-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h3>
        
        {% if post.excerpt %}
          <p class="entry-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
        {% endif %}
        
        <footer class="entry-meta">
          <time class="entry-time" datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%Y-%m-%d" }}
          </time>
          
          {% if post.tags.size > 0 %}
            <div class="entry-tags">
              {% for tag in post.tags %}
                <span class="tag">{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </footer>
      </div>
    </article>
  {% endfor %}
</div>
