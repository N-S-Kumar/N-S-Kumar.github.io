---
layout: page
permalink: /reflections/
title: reflections
nav: true
nav_order: 3
---

This section is for literature, philosophy, and personal reflection.

{% assign reflection_posts = site.posts | where_exp: "post", "post.categories contains 'reflections'" %}
{% for post in reflection_posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%B %d, %Y" }}_

{% if post.description %}{{ post.description }}{% endif %}

{% endfor %}
