---
layout: page
title: 哲思
permalink: /philosophy/
---

## 哲思文章 Thinking

<div style="background: #f8f9fa; padding: 1.5em; margin: 1.5em 0; border-radius: 8px; border-left: 4px solid #6c757d; color: #495057; line-height: 1.6;">
這裡的文章不是學術文章，而是一些我在生活中遇見的思考與疑問。或許不夠完整、不夠嚴謹，但都真實地來自我的經驗與感受。如果你也曾對某些事感到困惑，希望這些文字能陪你一起走一段思考的路。
</div>

{% assign posts = site.categories.philosophy %}
{% for post in posts %}
<article style="margin-bottom: 2em; border: 1px solid #eee; border-radius: 8px; overflow: hidden;">
  {% if post.image %}
    <div style="height: 200px; overflow: hidden;">
      <img src="{{ post.image }}" alt="{{ post.title }}" style="width: 100%; height: 100%; object-fit: cover;">
    </div>
  {% endif %}
  
  <div style="padding: 1.5em;">
    <h3 style="margin: 0 0 0.5em 0;">
      <a href="{{ post.url }}" style="text-decoration: none; color: #333;">{{ post.title }}</a>
    </h3>
    
    {% if post.excerpt %}
      <p style="color: #666; margin: 0 0 1em 0;">{{ post.excerpt | strip_html | truncate: 150 }}</p>
    {% endif %}
    
    <div style="display: flex; justify-content: space-between; align-items: center; color: #999; font-size: 0.9em;">
      <time>{{ post.date | date: "%Y-%m-%d" }}</time>
      
      {% if post.tags.size > 0 %}
        <div>
          {% for tag in post.tags %}
            <span style="background: #f0f0f0; padding: 0.2em 0.5em; border-radius: 3px; margin-left: 0.5em; font-size: 0.8em;">{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </div>
  </div>
</article>
{% endfor %}
