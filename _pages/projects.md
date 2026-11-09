---
layout: page
title: projects
permalink: /projects/
description: Selected research and open-source projects in reinforcement learning, knowledge graphs, and AI applications.
nav: true
nav_order: 2
display_categories: [research, LLM applications, computer vision]
horizontal: false
---

<div class="projects">
{% assign featured_projects = site.projects | where: "featured", true | sort: "importance" %}
{% if featured_projects.size > 0 %}
  <h2 class="category">featured projects</h2>
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in featured_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
{% endif %}
{% for category in page.display_categories %}
  {% assign sorted_projects = site.projects | where: "category", category | where_exp: "project", "project.featured != true" | sort: "importance" %}
  {% if sorted_projects.size > 0 %}
  <h2 class="category">{{ category }}</h2>
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endfor %}
</div>
