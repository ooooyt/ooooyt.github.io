---
layout: page
title: "AI"
permalink: /ai/
---

{% for post in site.categories.ai %}
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
