---
layout: page
permalink: /science/
title: science notes
nav: true
nav_order: 3
---

This section tracks my scientific pursuits and notes from talks in physics, math, and biology.

{% assign science_posts = site.posts | where_exp: "post", "post.categories contains 'science-notes'" %}
{% for post in science_posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%B %d, %Y" }}_

{% if post.description %}{{ post.description }}{% endif %}

{% endfor %}
