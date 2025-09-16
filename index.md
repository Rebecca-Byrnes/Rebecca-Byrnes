---
layout: default
---

## About Me

Hi, I’m Rebecca Byrnes. I work at the intersection of climate policy, data, and communication. I enjoy building clear, engaging tools and content that help people understand complex systems.

• Policy and research translation into visuals and stories
• Data analysis and interactive dashboards
• Writing and speaking on climate and markets

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

## Contact

I’m always open to collaborating or speaking.

- Email: <a href="mailto:rebecca@example.com">rebecca@example.com</a>
- LinkedIn: <a href="https://www.linkedin.com/in/rebeccabyrnes" target="_blank" rel="noopener">linkedin.com/in/rebeccabyrnes</a>
- GitHub: <a href="https://github.com/rebecca-byrnes" target="_blank" rel="noopener">github.com/rebecca-byrnes</a>
