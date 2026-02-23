---
layout: default
title: Все заметки
permalink: /blog/
---

<h1>Все заметки</h1>

<div class="blog-posts">
  {% for post in site.posts %}
    <article class="blog-post">
      <div class="post-preview" onclick="togglePost(this)">
        <h3 class="post-title">{{ post.title }}</h3>
        <div class="post-meta">
          <span>{{ post.date | date: "%d %B %Y" }}</span>
        </div>
        <div class="post-excerpt">
          {{ post.content | strip_html | truncatewords: 30 }}
        </div>
        <div class="expand-icon">▼</div>
      </div>
      <div class="post-full">
        <div class="post-content">
          {{ post.content }}
        </div>
      </div>
    </article>
  {% endfor %}
</div>