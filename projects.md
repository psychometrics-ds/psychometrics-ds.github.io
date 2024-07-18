---
layout: articles
title: Projects
articles:
  data_source: sorted_projects
  show_excerpt: true
  show_cover: false
  show_readmore: true
  excerpt_type: html
  show_info: true
---

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}

<!-- Debugging: Display the sorted projects list -->
{% for project in sorted_projects %}
  <p>{{ project.title }} - {{ project.date }}</p>
{% endfor %}