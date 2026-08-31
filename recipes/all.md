---
layout: null
---
{% assign page_dir = page.path | remove: page.name %}
{% for file in site.static_files %}{% if file.extname == '.yml' or file.extname == '.yaml' %}{% assign file_dir = file.path | remove: file.name | remove_first: '/' %}{% if file_dir == page_dir %}{{ file.name }}
{% endif %}{% endif %}{% endfor %}
