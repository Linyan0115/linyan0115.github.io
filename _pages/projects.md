---
layout: page
title: projects
permalink: /projects/
nav: true
nav_order: 3
---

{% assign undergraduate_projects = site.projects | where: "category", "work" | sort: "importance" %}
{% assign graduate_projects = site.projects | where: "category", "graduate" | sort: "importance" %}

<div class="projects">
  <h2 class="category" id="undergraduate-projects">Undergraduate Projects</h2>
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in undergraduate_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>

  <h2 class="category mt-4" id="graduate-projects">Graduate Projects</h2>
  {% if graduate_projects.size > 0 %}
    <div class="row row-cols-1 row-cols-md-3">
      {% for project in graduate_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  {% else %}
    <p><em>Coming soon.</em></p>
  {% endif %}
</div>
