---
layout: default
is_contact: true
title: Contact
---

# {{ page.title }}

{% if site.data.social %}
<div id="social-media">
    {% assign sm = site.data.social %}
    {% for entry in sm %}
        {% assign key = entry | first %}
        {% if sm[key].id %}
            <ul>{{ sm[key].title }} <a href="{{ sm[key].href }}{{ sm[key].id }}" title="{{ sm[key].title }}"><i class="fa {{ sm[key].fa-icon }}"></i></a></ul>
        {% endif %}
    {% endfor %}
</div>
{% endif %}
