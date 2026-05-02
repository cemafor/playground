---
layout: default
title: Site Index
---

# Site Index

A directory of all pages available in this repository.

---

## Pages

{% raw %}
<ul>
  {% for page in site.pages %}
    {% if page.name contains '.html' %}
      <li>
        <a href="{{ page.url | relative_url }}">{{ page.title | default: page.name }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
{% endraw %}

*Last updated: {{ site.time | date: "%B %d, %Y" }}*