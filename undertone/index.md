---
layout: page
title: "Undertone"
permalink: /undertone/
---

{% for post in site.categories.undertone %}
  <div class="post-preview">
    <a href="{{ post.url }}">
      <h2 class="post-title">{{ post.title }}</h2>
      {% if post.subtitle %}
        <h3 class="post-subtitle">{{ post.subtitle }}</h3>
      {% endif %}
    </a>
    <p class="post-meta">
      {{ post.date | date: "%B %d, %Y" }}
    </p>
    {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    {% endif %}
    <hr>
  </div>
{% endfor %}
