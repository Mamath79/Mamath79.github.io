---
layout: page
title: Développeur Concepteur Logiciel
description: Développeur Python certifié OpenClassrooms, spécialisé Django, bases de données & automatisation. Passionné par la conception logicielle robuste et la qualité de code.
image: assets/images/design_dev_1.jpg
banner_no_overlay: false
banner_fit: contain
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

      <p>
        Après 20 ans d’expérience en ingénierie du son, je me suis reconverti avec succès vers le 
        <strong>développement logiciel</strong>. Diplômé de la formation 
        <strong>Développeur d’application Python (niveau 6 RNCP)</strong> chez OpenClassrooms, 
        j’ai acquis une solide expertise en <strong>Python, Django, SQL et bonnes pratiques logicielles</strong>.  
        Mon approche combine rigueur technique et créativité, avec un accent fort sur la 
        <strong>qualité du code, les tests et l’architecture logicielle</strong>.
      </p>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">CV (FR)</a></li>
        <li><a href="mailto:contact@naxencia.fr" class="button icon fa-envelope">Contact</a></li>
      </ul>

      <hr class="major" />

      <h2>Portfolio Développeur</h2>
      <p class="small">Exemples de projets techniques réalisés dans le cadre de ma formation et de projets personnels.</p>

      <section class="tiles">
      {% assign items = site.data.portfolio_dev.projects %}
      {% for item in items %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic09.jpg') | relative_url }}" alt="{{ item.title }}">
          </span>
          <a href="#dev-{{ item.slug }}" class="link">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
            {% if item.stack %}<p><em>Stack:</em> {{ item.stack | join: ', ' }}</p>{% endif %}
            {% if item.blurb %}<p>{{ item.blurb }}</p>{% endif %}
          </a>
        </article>
        <div id="dev-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Fermer"></a>
          <div class="modal-content" style="background-image: url('{{ (item.image | default: '/assets/images/pic09.jpg') | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Fermer">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
              {% if item.role %}<p>{{ item.role }}</p>{% endif %}
              {% if item.stack %}<p><em>Stack:</em> {{ item.stack | join: ', ' }}</p>{% endif %}
              {% if item.blurb %}<p>{{ item.blurb }}</p>{% endif %}
              <div class="actions">
                {% if item.repo %}<a class="button" href="{{ item.repo }}" target="_blank" rel="noopener">Voir le code</a>{% endif %}
                {% if item.link %}<a class="button alt" href="{{ item.link }}" target="_blank" rel="noopener">Voir le site</a>{% endif %}
                <a class="button" href="#close">Fermer</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <div class="row">
        <div class="6u 12u$(medium)">
          <h3>Compétences techniques</h3>
          <ul>
            <li>Python, SQL, Django / Django REST Framework</li>
            <li>Architecture MVC, POO, design patterns</li>
            <li>Tests unitaires & intégration (pytest, coverage >80%)</li>
            <li>CI/CD avec GitHub Actions & Docker</li>
            <li>Bases de données relationnelles (MySQL, SQLite)</li>
          </ul>
        </div>
        <div class="6u$ 12u$(medium)">
          <h3>Outils & Workflow</h3>
          <ul>
            <li>Git/GitHub, GitHub Pages, Render</li>
            <li>VS Code, MySQL Workbench, Docker</li>
            <li>Sphinx / Read the Docs (documentation)</li>
            <li>Agile / Scrum (trello, user stories)</li>
          </ul>
        </div>
      </div>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV_Mathieu_Vieillefont_Developpeur_FR.pdf' | relative_url }}" class="button special icon fa-download">Télécharger le CV</a></li>
        <li><a href="mailto:contact@naxencia.fr" class="button icon fa-calendar">Proposer un projet</a></li>
      </ul>
    </div>
  </section>
</div>
