---
layout: post
title: "GitHub Pages 个人博客搭建指南"
date: 2026-05-20 14:00:00 +0800
categories: 教程
---

这是一篇手把手教你用 GitHub Pages 搭建个人博客的教程。

## 什么是 GitHub Pages

GitHub Pages 是 GitHub 提供的免费静态网站托管服务，支持 Jekyll 框架，可以轻松搭建个人博客、项目文档等。

## 搭建步骤

### 1. 创建仓库

打开 GitHub，创建一个名为 `用户名.github.io` 的公开仓库。

### 2. 本地初始化

```bash
mkdir username.github.io
cd username.github.io
git init
```

### 3. 配置 Jekyll

创建 `_config.yml`、`_layouts`、`_posts` 等目录和文件。

### 4. 推送上线

```bash
git add -A
git commit -m "初始化博客"
git push -u origin master
```

### 5. 开启 Pages

仓库 Settings → Pages → 选择 master 分支即可。

## 写新文章

在 `_posts` 目录下创建 `YYYY-MM-DD-标题.md`，格式：

```yaml
---
layout: post
title: "文章标题"
date: 2026-05-20
categories: 分类
---

正文内容...
```

推送后自动部署，无需手动操作。

## 总结

GitHub Pages + Jekyll 是目前最简单、免费的博客方案之一，适合开发者快速搭建个人站点。
