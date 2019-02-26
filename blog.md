---
layout: page
title: Blog Posts
permalink: /blog/
---

<div class="post-list">
{% for post in site.categories.blog %}
  <div class="post">
    {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
    <span class="post-meta">{{ post.date | date: date_format }}</span>

    <h2>
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    </h2>
    {{ post.excerpt }}
  </div>
  {% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
</div>
