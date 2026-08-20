---
layout: page
title: Projects
permalink: /projects/
---
# Projects

<div class="page-intro">Research projects and ongoing directions.</div>

<div class="project-grid">
{% for project in site.data.projects %}
  <article class="project-card">
    <div class="project-period">{{ project.period }}</div>
    <h2>{{ project.title }}</h2>
    <p>{{ project.description }}</p>
    {% if project.link and project.link != '' %}<a class="text-link" href="{{ project.link }}">Learn more →</a>{% endif %}
  </article>
{% endfor %}
</div>
