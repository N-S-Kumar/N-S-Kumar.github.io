---
layout: page
permalink: /blog/
title: all writing
nav: true
nav_order: 2
---

This is the complete archive of my writing across both streams.

- [Science Notes](/science/)
- [Reflections](/reflections/)

---

{% for post in site.posts %}
  {% unless post.categories contains "sample-posts" %}
    <article style="margin-bottom: 1.75rem;">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p style="margin: 0.2rem 0;">
        {{ post.date | date: "%B %d, %Y" }}
        {% if post.categories %}
          · {{ post.categories | join: ", " }}
        {% endif %}
      </p>
      {% if post.description %}
        <p>{{ post.description }}</p>
      {% endif %}
    </article>
  {% endunless %}
{% endfor %}
