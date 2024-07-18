---
layout: page
title: Projects
---

<!-- Debugging: Display the projects object -->
{{ site.projects | inspect }}

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}

<div class="layout--articles">
  <div class="article-list items">
    {% for project in sorted_projects %}
      <article class="item">
        <header>
          <a href="{{ project.url }}"><h2>{{ project.title }}</h2></a>
        </header>
        <div class="item__content">
          <p>{{ project.date }}</p>
          <p>{{ project.excerpt }}</p>
        </div>
      </article>
    {% endfor %}
  </div>
</div>