---
layout: default
title: Projects
permalink: /projects/
---

## Projects

<div class="projects-grid">
  {% for project in site.data.projects %}
  <article class="project-card">
    {% if project.image %}
    <div class="project-image" style="background-image: url('{{ project.image }}');"></div>
    {% endif %}
    <div class="project-content">
      <h3 class="project-title">{{ project.title }}</h3>
      <p class="project-desc">{{ project.description }}</p>
      {% if project.tags %}
      <div class="project-tags">
        {% for tag in project.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
      <div class="project-links">
        {% if project.live_url %}
        <a class="button" href="{{ project.live_url }}" target="_blank" rel="noopener">Live</a>
        {% endif %}
        {% if project.repo_url %}
        <a class="button ghost" href="{{ project.repo_url }}" target="_blank" rel="noopener">Code</a>
        {% endif %}
      </div>
    </div>
  </article>
  {% endfor %}
  {% if site.data.projects == nil or site.data.projects.size == 0 %}
  <p>Add your projects in <code>_data/projects.yml</code> to populate this section.</p>
  {% endif %}
</div>


