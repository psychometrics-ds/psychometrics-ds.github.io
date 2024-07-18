---
layout: articles
title: Projects
articles:
  data_source: site.projects | sort: 'date' | reverse
  show_excerpt: true
  show_cover: false
  show_readmore: true
  excerpt_type: html
  show_info: true
---

<!-- Debugging: Display the sorted projects list -->
{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
  <p>{{ project.title }} - {{ project.date }}</p>
{% endfor %}