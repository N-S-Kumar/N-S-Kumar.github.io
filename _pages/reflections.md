---
layout: page
permalink: /reflections/
title: reflections
nav: true
nav_order: 4
---

This section is for my literature and philosophy notes, along with personal reflections and regular updates.

{% assign reflection_posts = site.posts | where_exp: "post", "post.categories contains 'reflections'" %}
{% for post in reflection_posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%B %d, %Y" }}_

{% if post.description %}{{ post.description }}{% endif %}

{% endfor %}
