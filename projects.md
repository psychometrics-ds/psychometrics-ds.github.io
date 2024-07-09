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
  group_by: year
  reverse: false
---

<div class="js-result layout--archive__result d-none">
  {%- include article-list.html articles=site.projects excerpt_type: html show_excerpt: true show_readmore: true show_cover: false show_info=true reverse=true group_by='year' -%}
</div>