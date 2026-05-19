---
layout: default
title: 首页
---

# 欢迎来到我的博客 🎉

这里是 **qingxuan-Mu** 的个人博客，记录技术学习与日常思考。

## 最新文章

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li>
      <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

[查看所有文章 →](/archive)
