---
layout: page
titles: People
---

<div class="layout--archive js-all">
  <div class="js-result layout--archive__result d-none">
    {%- include article-list.html articles=site.people type='brief' show_info=true reverse=true -%}
  </div>
</div>

{{ content }}
