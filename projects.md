---
layout: page
title: Projects
---

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}

<div class="layout--articles">
  <div class="article-list items items--divided">
    {% for project in sorted_projects %}
      <article class="item">
        <header>
          <a href="{{ project.url }}"><h2>{{ project.title }}</h2></a>
        </header>
        <div class="item__content">
          <p>{{ project.date }}</p>
          <div class="article__content">
            {{ project.excerpt | strip_html | strip | truncate: 350 }}
          </div>
          <p><a href="{{ project.url }}">Read more</a></p>
        </div>
      </article>
    {% endfor %}
  </div>
</div>