---
layout: default
title: Blog
---

# Blog

<section class="post-list">
  {% for post in site.posts %}
    <article>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div>
        <b>Posted on:</b> {{ post.date }}
        <b>Tags:</b> {{ post.tags }}
      </div>
      {{ post.excerpt }}
    </article>
  {% endfor %}
</section>
