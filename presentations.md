---
layout: default
title: Presentations
---

# {{ page.title }}

<ul>
  {% for post in site.posts %}
    {% if post.layout == "presentation" %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>