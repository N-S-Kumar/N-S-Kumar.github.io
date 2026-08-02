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
  <article style="margin-bottom: 1.75rem;">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p style="margin: 0.2rem 0;">{{ post.date | date: "%B %d, %Y" }}</p>
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}
