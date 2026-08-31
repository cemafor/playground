---
layout: null
permalink: /yaml-files.txt
---
{% for file in site.static_files %}{% if file.extname == '.yml' or file.extname == '.yaml' %}{{ file.path }}
{% endif %}{% endfor %}
