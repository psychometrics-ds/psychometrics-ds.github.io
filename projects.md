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