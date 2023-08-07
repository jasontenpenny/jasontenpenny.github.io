---
layout: default
title: Blog
---

<section class="post-list">
  {% for post in site.posts %}
    <article class="post-entry">
      <h3 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div class="post-metadata">
        <b>Posted on:</b> {{ post.date | date: '%B %d, %Y' }}<br />
        <b>Tags:</b> {% for tag in post.tags %}{{ tag | replace: "+", " " }}, {% endfor %}
      </div>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
    </article>
  {% endfor %}
</section>
