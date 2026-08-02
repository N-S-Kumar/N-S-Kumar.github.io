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
  <article style="margin-bottom: 1.75rem;">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p style="margin: 0.2rem 0;">{{ post.date | date: "%B %d, %Y" }}</p>
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}
