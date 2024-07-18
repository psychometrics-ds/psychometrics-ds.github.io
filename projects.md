---
layout: articles
title: Projects
articles:
  data_source: projects_sorted
  show_excerpt: true
  show_cover: false
  show_readmore: true
  excerpt_type: html
  show_info: true
---

{% assign projects_sorted = site.projects | sort: 'date' | reverse %}

<!-- Debugging: Display the sorted projects list -->
{% for project in projects_sorted %}
  <p>{{ project.title }} - {{ project.date }}</p>
{% endfor %}