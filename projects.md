---
layout: page
titles: Projects
---

<div class="layout--archive js-all">
  <div class="js-result layout--archive__result d-none">
    {%- include article-list.html articles=site.projects type='brief' show_info=true reverse=true group_by='year' -%}
  </div>
</div>

{{ content }}