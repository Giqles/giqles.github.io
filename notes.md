---
layout: default
title: Notes
---

# {{ page.title }}

<ul>
  {% for post in site.posts %}
    {% if post.layout == "default" %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>