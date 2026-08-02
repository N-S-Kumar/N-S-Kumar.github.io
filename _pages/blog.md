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

### [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%B %d, %Y" }}{% if post.categories %} · {{ post.categories | join: ", " }}{% endif %}_

{% if post.description %}{{ post.description }}{% endif %}

{% endunless %}
{% endfor %}
