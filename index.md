---
layout: default
---

## About Me

Hi, I’m Rebecca Byrnes — a cybersecurity and information security compliance professional based in Portugal. I help organizations design, implement, and mature security programs that are practical, auditable, and aligned to business goals.

• ISO/IEC 27001 implementation and internal audits
• SOC 2 readiness, control design, and evidence collection
• Risk management aligned to ISO 27005 and NIST

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

I’m open to consulting, full‑time roles, and collaborations.

- Email: <a href="mailto:rebecca@rebeccabyrnes.site">rebecca@rebeccabyrnes.site</a>
- LinkedIn: <a href="https://www.linkedin.com/in/rebeccabyrnes" target="_blank" rel="noopener">linkedin.com/in/rebeccabyrnes</a>
- GitHub: <a href="https://github.com/Rebecca-Byrnes" target="_blank" rel="noopener">github.com/Rebecca-Byrnes</a>
