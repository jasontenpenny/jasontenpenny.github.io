---
layout: default
title: Blog
---

# Blog

<section class="post-list">
  {% for post in site.posts %}
    <article class="post-entry">
      <h3 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div class="post-metadata">
        <b>Posted on:</b> {{ post.date }}<br />
        <b>Tags:</b> {{ post.tags }}
      </div>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
    </article>
  {% endfor %}
</section>
