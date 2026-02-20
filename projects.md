---
layout: default
title: Projects
---

{% include nav.html %}

# Projects

{% assign items = site.projects | sort: "order" %}

<div class="projects-grid">
  {% for project in items %}
    <a href="{{ site.baseurl }}{{ project.url }}" class="project-item">
      {% if project.category %}
        <div class="project-meta">
          <span class="project-tag">{{ project.category }}</span>
        </div>
      {% endif %}

      <h3>{{ project.title }}</h3>

      {% if project.summary %}
        <p>{{ project.summary }}</p>
      {% elsif project.one_liner %}
        <p>{{ project.one_liner }}</p>
      {% elsif project.subtitle %}
        <p>{{ project.subtitle }}</p>
      {% endif %}

      <span class="project-link">View Case Study →</span>
    </a>
  {% endfor %}
</div>
