---
layout: articles
title: Projects
articles:
  data_source: site.projects
  show_excerpt: true
  show_cover: false
  show_readmore: true
  excerpt_type: html
  show_info: true
---

{%- assign sorted_projects = site.projects | sort: 'date' | reverse -%}

{% for project in sorted_projects %}
  {% include article-item.html article=project %}
{% endfor %}