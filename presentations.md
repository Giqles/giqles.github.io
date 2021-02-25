---
layout: default
title: Presentations
---

# {{ page.title }}

<ul>
  {% for post in site.posts %}
    {% if post.layout == "presentation" %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>, 
        <a href='{{ site.url | append: "/assets/" | append: post.pdf_file }}'>[pdf]</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>