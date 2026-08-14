---
layout: default
title: Blog
permalink: /blog/
---

<h1>Blog</h1>

<div class="blog-archive">
  {% for post in site.posts %}
    <article class="blog-entry">
      <a class="blog-date" href="{{ post.url | relative_url }}">
        {{ post.date | date: "%d-%m-%Y" }}
      </a>

      <a class="blog-title" href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </article>
  {% endfor %}
</div>
