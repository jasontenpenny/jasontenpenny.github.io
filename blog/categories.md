---
layout: default
title: "Post Categories"
---

<section class="category-list">
    {% for category in site.categories %}
    {% if category != "blog" %}
    <section class="category-entry">
        <h2 class="category-title" id="{{ category[0] | url_encode}}">{{ category[0] }}</h2>
        {% for post in category[1] %}
        <article class="post-entry">
            <h3 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <div class="post-metadata">
                <b>Posted on:</b> {{ post.date | date: '%B %d, %Y' }}<br />
                <b>Tags:</b> {% for tag in post.tags -%}
                    {%- if forloop.length > 0 -%}
                        {{ tag | replace: "+", " " }}{% unless forloop.last %}, {% endunless -%}
                    {%- endif -%}
                {% endfor %}
            </div>
        </article>
        {% endfor %}
    </section>
    {% endif %}
    {% endfor %}
</section>
