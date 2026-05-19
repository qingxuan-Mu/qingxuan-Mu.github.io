---
layout: default
title: 首页
---

<div class="hero">
  <div class="hero-badge"><i class="fas fa-feather-alt"></i> 个人博客</div>
  <h1>记录 <span class="highlight">技术与生活</span></h1>
  <p>用文字沉淀编程路上的思考与收获，持续成长，不断探索。</p>
  <div class="hero-stats">
    <div class="stat">
      <span class="stat-num">{{ site.posts.size }}</span>
      <span class="stat-label">文章</span>
    </div>
    <div class="stat">
      <span class="stat-num">{{ site.posts | map: "categories" | uniq | size }}</span>
      <span class="stat-label">分类</span>
    </div>
    <div class="stat">
      <span class="stat-num">{{ site.posts | size | plus: 0 }}</span>
      <span class="stat-label">发布</span>
    </div>
  </div>
</div>

<div class="container">
  <div class="section-header">
    <h2><i class="fas fa-pen-fancy" style="color:var(--accent);margin-right:6px;"></i> 最新文章</h2>
    <span class="section-line"></span>
    <a href="/archive" class="section-more">查看全部 →</a>
  </div>

  <div class="post-grid">
    {% for post in site.posts limit:5 %}
    <a class="post-card" href="{{ post.url | relative_url }}">
      <div class="card-meta">
        <span class="card-date"><i class="far fa-calendar-alt"></i> {{ post.date | date: "%Y-%m-%d" }}</span>
        {% if post.categories %}
        <span class="card-category"><i class="fas fa-tag"></i> {{ post.categories | first }}</span>
        {% endif %}
      </div>
      <div class="card-title">{{ post.title }}</div>
      {% if post.excerpt %}
      <div class="card-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</div>
      {% endif %}
    </a>
    {% endfor %}
  </div>
</div>
