---
layout: default
title: Blog
---

# Blog

<section class="post-list>
  {% for post in site.posts %}
    <article>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <details>
        <b>Posted on:</b> {{ post.date }}
        <b>Tags: {{ page.tags }}
      </details>
      {{ post.excerpt }}
    </article>
  {% endfor %}
</section>
