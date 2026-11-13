---
layout: page
title: Projects
permalink: /projects/
nav: true
nav_order: 3
---

{% assign graduate_projects = site.projects | where: "category", "graduate" | sort: "importance" %}
{% assign undergraduate_projects = site.projects | where: "category", "work" | sort: "importance" %}

<style>
  .projects .project-intro,
  .projects .project-section-heading,
  .projects .project-placeholder {
    color: var(--global-text-color);
    opacity: 1;
  }

  .projects .project-intro {
    max-width: 65ch;
    margin-bottom: 2rem;
    line-height: 1.65;
  }

  .projects .project-section-heading {
    font-size: 1.45rem;
    font-weight: 600;
    margin-bottom: 0.75rem;
  }

  .projects .project-placeholder {
    margin-bottom: 0;
  }
</style>

<div class="projects">

  <section aria-labelledby="graduate-projects">
    <h2 class="project-section-heading" id="graduate-projects">Graduate Projects</h2>
    {% if graduate_projects.size > 0 %}
      <div class="row row-cols-1 row-cols-md-3">
        {% for project in graduate_projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% else %}
      <p class="project-placeholder">Coming soon.</p>
    {% endif %}
  </section>

  <section class="mt-4" aria-labelledby="undergraduate-projects">
    <h2 class="project-section-heading" id="undergraduate-projects">Undergraduate Projects</h2>
    <div class="row row-cols-1 row-cols-md-3">
      {% for project in undergraduate_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  </section>
</div>
