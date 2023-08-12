---
layout: default
title: "Post Tags"
---

<section class="tag-list">
    <ul>
    {% for tag in site.tags %}
        <li><a href="#{{ tag[0] }}">{{ tag[0] | replace: "+", " " }}</a></li>
    {% endfor %}
    </ul>
    <div class="spacer">&nbsp;</div>
    {% for tag in site.tags %}
    <section class="tag-entry">
        <h2 class="tag-title" id="{{ tag[0] }}">{{ tag[0] | replace: "+", " " }}</h2>
        {% for post in tag[1] %}
        <article class="post-entry">
            <h3 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <div class="post-metadata">
                <b>Posted on:</b> {{ post.date | date: '%B %d, %Y' }}<br />
                <b>Category:</b> <a href="/blog/categories#{{ post.category | url_encode }}">{{ post.category }}</a>
            </div>
        </article>
        {% endfor %}
    </section>
    {% endfor %}
</section>
