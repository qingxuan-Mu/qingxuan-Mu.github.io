---
layout: default
title: 归档
---

<div class="archive-page">
  <h1><i class="fas fa-archive" style="color:var(--accent)"></i> 文章归档</h1>

  {% assign posts_by_year = site.posts | group_by_exp:"post","post.date | date: '%Y'" %}
  {% for year in posts_by_year %}
  <div class="archive-year">
    <h2>{{ year.name }}</h2>
    {% for post in year.items %}
    <div class="archive-item">
      <span class="archive-date">{{ post.date | date: "%m-%d" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>
    {% endfor %}
  </div>
  {% endfor %}

  {% if site.posts.size == 0 %}
  <p style="text-align:center;color:var(--text-muted);padding:3rem 0;">还没有文章，敬请期待 ✨</p>
  {% endif %}
</div>
