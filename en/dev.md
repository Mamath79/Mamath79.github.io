---
layout: page
lang: en
translation_key: dev
title: Developer Portfolio
description: A former sound engineer turned Python developer, delivering robust back-end services, automation, and CI/CD pipelines with a focus on code quality and documentation.
image: assets/images/design_dev_1.jpg
banner_no_overlay: false
banner_fit: contain
banner_compact: true
nav-menu: true
show_tile: true
tile_order: 1
permalink: /en/dev/
---

<!-- Main -->
<div id="main" class="alt">
  <section id="one">
    <div class="inner">
      <header class="major">
      </header>
      
      <div class="row">
        <div class="6u 12u$(medium)">
          <h3>Technical skills</h3>
          <ul>
            <li>Python, SQL, Django / Django REST Framework — secure, maintainable APIs.</li>
            <li>MVC architecture, OOP, design patterns — solid foundations to evolve your products.</li>
            <li>Unit & integration testing (pytest, coverage &gt;80%) — code verified continuously.</li>
            <li>CI/CD with GitHub Actions & Docker — smooth, controlled releases.</li>
            <li>Relational databases (MySQL, SQLite) — optimized schemas and efficient queries.</li>
          </ul>
        </div>
        <div class="6u$ 12u$(medium)">
          <h3>Workflow & tooling</h3>
          <ul>
            <li>Git/GitHub, GitHub Pages, Render — transparent versioning and deployments.</li>
            <li>VS Code, MySQL Workbench, Docker — productive environment for rapid prototyping.</li>
            <li>Sphinx / Read the Docs — living, accessible documentation.</li>
            <li>Agile / Scrum (Trello, user stories) — iterative delivery with clear visibility.</li>
          </ul>
        </div>
      </div>

      <section class="services-dev">
        <h2>Development services</h2>
        <div class="row">
          <div class="6u 12u$(medium)">
            <div class="box service-card">
              <h3>Django APIs & back ends</h3>
              <p>Designing secure, well-documented REST architectures with automated Docker/Render deployment.<br>Goal: reliable, scalable services you can maintain over time.</p>
            </div>
          </div>
          <div class="6u$ 12u$(medium)">
            <div class="box service-card">
              <h3>Python automation</h3>
              <p>Internal scripts and tooling to orchestrate workflows, streamline repetitive tasks, and save time.</p>
            </div>
          </div>
          <div class="6u 12u$(medium)">
            <div class="box service-card">
              <h3>CI/CD & deployment</h3>
              <p>GitHub Actions pipelines, continuous integration, and controlled releases.<br>Every project is tested and validated before production.</p>
            </div>
          </div>
          <div class="6u$ 12u$(medium)">
            <div class="box service-card">
              <h3>Dashboards & data</h3>
              <p>Interactive dashboards to monitor activity, reporting, or data visualisation.</p>
            </div>
          </div>
        </div>
      </section>

      <section id="portfolio-projects" class="tiles tiles--contain">
      <p>Here is a selection of projects that showcase my technical progression and quality-driven mindset.</p>
      {% assign items = site.data.portfolio_dev_en.projects %}
      {% for item in items %}
        <article>
          <span class="image">
            <img src="{{ item.image | default: '/assets/images/pic09.jpg' | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Python developer project' }}" loading="lazy" decoding="async">
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
          </header>
          <a href="#dev-{{ item.slug }}" class="link primary" aria-label="Open {{ item.title }}"></a>
        </article>
        <div id="dev-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Close"></a>
          <div class="modal-content" style="background-image: url('{{ item.image | default: '/assets/images/pic09.jpg' | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Close">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
              {% if item.role %}<p>{{ item.role }}</p>{% endif %}
              {% if item.stack %}<p><em>Stack:</em> {{ item.stack | join: ', ' }}</p>{% endif %}
              {% if item.blurb %}<p>{{ item.blurb }}</p>{% endif %}
              {% if item.result %}<p class="project-result"><strong>Impact:</strong> {{ item.result }}</p>{% endif %}
              <div class="actions">
                {% if item.repo %}<a class="button" href="{{ item.repo }}" target="_blank" rel="noopener">View the code</a>{% endif %}
                {% assign link_clean = item.link | default: '' | strip %}
                {% if link_clean != '' %}<a class="button alt" href="{{ link_clean }}" target="_blank" rel="noopener">Visit the project</a>{% endif %}
                <a class="button icon fa-envelope" href="mailto:{{ site.email }}">Contact me</a>
                <a class="button alt" href="#portfolio-projects">Back to projects</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>
      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">Download résumé (FR)</a></li>
        <li><a href="mailto:{{ site.email }}" class="button icon fa-paper-plane">Discuss a project</a></li>
      </ul>
    </div>
  </section>
</div>
