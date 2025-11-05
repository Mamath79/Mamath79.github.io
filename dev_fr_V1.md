---
layout: page
lang: fr
translation_key: dev
title: Portfolio Développeur
description: Après 20 ans d’expérience en ingénierie du son, je me suis reconverti avec succès vers le développement logiciel. Diplômé de la formation Développeur d’application Python (niveau 6 RNCP) chez OpenClassrooms, j’ai acquis une solide expertise en Python, Django, SQL et bonnes pratiques logicielles. Mon approche combine rigueur technique et créativité, avec un accent fort sur la qualité du code, les tests et l’architecture logicielle.
image: assets/images/design_dev_1.jpg
banner_no_overlay: false
banner_fit: contain
banner_compact: true
nav-menu: true
show_tile: true
tile_order: 1
---

<!-- Main -->
<div id="main" class="alt">
  <section id="one">
    <div class="inner">
      <header class="major">
      </header>
      
      <div class="row">
        <div class="6u 12u$(medium)">
          <h3>Compétences techniques</h3>
          <ul>
            <li>Python, SQL, Django / Django REST Framework — APIs sécurisées et maintenables.</li>
            <li>Architecture MVC, POO, design patterns — bases solides pour faire évoluer vos produits.</li>
            <li>Tests unitaires & intégration (pytest, coverage &gt;80%) — code validé en continu.</li>
            <li>CI/CD avec GitHub Actions & Docker — livraisons fluides et maîtrisées.</li>
            <li>Bases de données relationnelles (MySQL, SQLite) — schémas optimisés et requêtes performantes.</li>
          </ul>
        </div>
        <div class="6u$ 12u$(medium)">
          <h3>Outils & Workflow</h3>
          <ul>
            <li>Git/GitHub, GitHub Pages, Render — suivi clair des versions et déploiements.</li>
            <li>VS Code, MySQL Workbench, Docker — environnement outillé pour prototyper vite.</li>
            <li>Sphinx / Read the Docs — documentation vivante et accessible.</li>
            <li>Agile / Scrum (Trello, user stories) — progression itérative, visibilité à chaque étape.</li>
          </ul>
        </div>
      </div>

      <section class="services-dev">
        <h2>Services développement</h2>
        <div class="row">
          <div class="6u 12u$(medium)">
            <div class="box service-card">
              <h3>API & back-ends Django</h3>
              <p>Conception d’architectures REST sécurisées et documentées, déploiement automatisé avec Docker et Render.<br>Objectif&nbsp;: des services fiables, scalables et maintenables dans le temps.</p>
            </div>
          </div>
          <div class="6u$ 12u$(medium)">
            <div class="box service-card">
              <h3>Automatisation Python</h3>
              <p>Scripts et outils internes pour orchestrer vos flux, simplifier vos tâches récurrentes et gagner du temps.</p>
            </div>
          </div>
          <div class="6u 12u$(medium)">
            <div class="box service-card">
              <h3>CI/CD & déploiement</h3>
              <p>Pipelines GitHub Actions, intégration continue, livraison contrôlée.<br>Chaque projet est testé et validé avant mise en production.</p>
            </div>
          </div>
          <div class="6u$ 12u$(medium)">
            <div class="box service-card">
              <h3>Dashboards & data</h3>
              <p>Tableaux de bord interactifs pour piloter vos données (analyses, reporting, visualisations).</p>
            </div>
          </div>
        </div>
      </section>

      <section id="portfolio-projects" class="tiles tiles--contain">
      <p>Voici une sélection de projets illustrant ma progression technique et mon approche orientée qualité logicielle.</p>
      {% assign items = site.data.portfolio_dev.projects %}
      {% for item in items %}
        <article>
          <span class="image">
            <img src="{{ item.image | default: '/assets/images/pic09.jpg' | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Projet développeur Python' }}" loading="lazy" decoding="async">
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
          </header>
          <a href="#dev-{{ item.slug }}" class="link primary" aria-label="Ouvrir {{ item.title }}"></a>
        </article>
        <div id="dev-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Fermer"></a>
          <div class="modal-content" style="background-image: url('{{ item.image | default: '/assets/images/pic09.jpg' | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Fermer">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client %}<p><strong>Client&nbsp;:</strong> {{ item.client }}</p>{% endif %}
              {% if item.role %}<p>{{ item.role }}</p>{% endif %}
              {% if item.stack %}<p><em>Stack&nbsp;:</em> {{ item.stack | join: ', ' }}</p>{% endif %}
              {% if item.blurb %}<p>{{ item.blurb }}</p>{% endif %}
              {% if item.result %}<p class="project-result"><strong>Impact&nbsp;:</strong> {{ item.result }}</p>{% endif %}
              <div class="actions">
                {% if item.repo %}<a class="button" href="{{ item.repo }}" target="_blank" rel="noopener">Voir le code</a>{% endif %}
                {% assign link_clean = item.link | default: '' | strip %}
                {% if link_clean != '' %}<a class="button alt" href="{{ link_clean }}" target="_blank" rel="noopener">Voir le site</a>{% endif %}
                <a class="button icon fa-envelope" href="mailto:{{ site.email }}">Me contacter</a>
                <a class="button alt" href="#portfolio-projects">Voir tous les projets</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>
      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">Télécharger le CV</a></li>
        <li><a href="mailto:{{ site.email }}" class="button icon fa-paper-plane">Discuter d'un projet</a></li>
      </ul>
    </div>
  </section>
</div>
