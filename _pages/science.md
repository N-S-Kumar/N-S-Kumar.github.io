---
layout: page
title: science notes
permalink: /science/
nav: true
nav_order: 5
---

This section collects writing on biology, physics, mathematics, and quantitative ideas.

{% assign science_posts = site.posts | where_exp: "post", "post.categories contains 'science-notes'" %}
{% for post in science_posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

_{{ post.date | date: "%B %d, %Y" }}_

{% if post.description %}{{ post.description }}{% endif %}

{% endfor %}
