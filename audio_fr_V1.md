---
layout: page
title: Portfolio Ingénieur du son.
description: Enregistrement, Montage & Mixage. Doublage, Post-production audiovisuelle. 20 ans d’expérience.
image: assets/images/DSC00243-small-34.jpg
banner_no_overlay: false
banner_fit: contain
nav-menu: true
show_tile: true
tile_order: 2
---

<!-- Main -->
<div id="main" class="alt">
  <section id="one">
    <div class="inner">
      <header class="major">
      </header>

      <div class="box audio-summary">
        <p><strong>+20&nbsp;ans</strong> d’ingénierie du son | Doublage, montage & mixage VF | Workflow remote sécurisé.</p>
        <p><strong>Studios&nbsp;:</strong> Dubbing Brothers, Iyuno, TitraFilm | <strong>Plateformes&nbsp;:</strong> Netflix, Disney+, Apple TV+, Prime Video.</p>
      </div>

      <nav class="audio-toc">
        <ul>
          <li><a href="#audio-cinema-rec">Cinéma — Enregistrement</a></li>
          <li><a href="#audio-cinema-mix">Cinéma — Mixage</a></li>
          <li><a href="#audio-series">Séries TV / TV films</a></li>
        </ul>
      </nav>

      <p>
        Ingénieur du son depuis plus de 20 ans, j’ai accompagné de nombreuses productions (cinéma, séries, documentaires) dans les studios parisiens les plus reconnus.
      </p>
      <p>
        J’interviens en enregistrement, montage et mixage, avec une approche rigoureuse et créative.
      </p>
      <p>
        Mon expérience en post-production dialogue s’articule parfaitement avec ma pratique du développement logiciel&nbsp;: automatisation des flux, optimisation des workflows et qualité de rendu.
      </p>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">CV (FR)</a></li>
        <li><a href="mailto:{{ site.email }}" class="button icon fa-paper-plane">Discuter d'un projet</a></li>
      </ul>

      <hr class="major" />

      <h2>Portfolio (sélection)</h2>
      <p class="small">Quelques projets marquants, où la précision technique et la direction artistique se rejoignent.</p>
      <p class="small">Clique sur une vignette pour afficher les détails.</p>

      <!-- TILES: Cinéma — Enregistrement -->
      <h2 id="audio-cinema-rec">Cinéma — Enregistrement</h2>
      <section class="tiles tiles--contain">
      {% for item in site.data.portfolio_audio.cinema_rec %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic01.jpg') | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Projet audio' }}" loading="lazy" decoding="async" />
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client&nbsp;:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
          </header>
          <a href="#audio-{{ item.slug }}" class="link primary" aria-label="Voir {{ item.title }}"></a>
        </article>
        <div id="audio-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Fermer"></a>
          <div class="modal-content" style="background-image: url('{{ (item.image | default: '/assets/images/pic01.jpg') | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Fermer">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client or item.doubleur %}
              <p>
                Pour ce projet, j'ai réalisé
                {% if item.role %}{{ item.role | downcase }}{% else %}mon intervention{% endif %}
                {% if item.doubleur %}
                  chez <a href="{{ item.doubleur }}" target="_blank" rel="noopener">
                    {{ item.doubleur | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}
                {% if item.client %}
                  pour <a href="{{ item.client }}" target="_blank" rel="noopener">
                    {{ item.client | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}.
              </p>
              {% endif %}
              <div class="actions">
                {% if item.link %}<a class="button" href="{{ item.link }}" target="_blank" rel="noopener">Voir la fiche</a>{% endif %}
                <a class="button alt" href="#close">Fermer</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <!-- TILES: Cinéma — Mixage -->
      <h2 id="audio-cinema-mix">Cinéma — Mixage</h2>
      <section class="tiles tiles--contain">
      {% for item in site.data.portfolio_audio.cinema_mix %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic03.jpg') | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Projet audio' }}" loading="lazy" decoding="async" />
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client&nbsp;:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
          </header>
          <a href="#audio-{{ item.slug }}" class="link primary" aria-label="Voir {{ item.title }}"></a>
        </article>
        <div id="audio-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Fermer"></a>
          <div class="modal-content" style="background-image: url('{{ (item.image | default: '/assets/images/pic03.jpg') | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Fermer">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client or item.doubleur %}
              <p>
                Pour ce projet, j'ai réalisé
                {% if item.role %}{{ item.role | downcase }}{% else %}mon intervention{% endif %}
                {% if item.doubleur %}
                  chez <a href="{{ item.doubleur }}" target="_blank" rel="noopener">
                    {{ item.doubleur | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}
                {% if item.client %}
                  pour <a href="{{ item.client }}" target="_blank" rel="noopener">
                    {{ item.client | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}.
              </p>
              {% endif %}
              <div class="actions">
                {% if item.link %}<a class="button" href="{{ item.link }}" target="_blank" rel="noopener">Voir la fiche</a>{% endif %}
                <a class="button alt" href="#close">Fermer</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <!-- TILES: Séries Tv / Tv films -->
      <h2 id="audio-series">Séries TV / TV films</h2>
      <section class="tiles tiles--contain">
      {% for item in site.data.portfolio_audio.series %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic05.jpg') | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Projet audio' }}" loading="lazy" decoding="async" />
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client&nbsp;:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
          </header>
          <a href="#audio-{{ item.slug }}" class="link primary" aria-label="Voir {{ item.title }}"></a>
        </article>
        <div id="audio-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Fermer"></a>
          <div class="modal-content" style="background-image: url('{{ (item.image | default: '/assets/images/pic05.jpg') | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Fermer">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client or item.doubleur %}
              <p>
                Pour ce projet, j'ai réalisé
                {% if item.role %}{{ item.role | downcase }}{% else %}mon intervention{% endif %}
                {% if item.doubleur %}
                  chez <a href="{{ item.doubleur }}" target="_blank" rel="noopener">
                    {{ item.doubleur | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}
                {% if item.client %}
                  pour <a href="{{ item.client }}" target="_blank" rel="noopener">
                    {{ item.client | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}.
              </p>
              {% endif %}
              <div class="actions">
                {% if item.link %}<a class="button" href="{{ item.link }}" target="_blank" rel="noopener">Voir la fiche</a>{% endif %}
                <a class="button alt" href="#close">Fermer</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <div class="row">
        <div class="6u 12u$(medium)">
          <h3>Compétences clés</h3>
          <ul>
            <li>Montage & Mixage&nbsp;: Pro Tools, ADR, VO, FX, musique.</li>
            <li>Workflow & automatisation&nbsp;: templates, macros, scripts personnalisés.</li>
            <li>Clients & studios&nbsp;: Dubbing Brothers, TitraFilm, Iyuno, Deluxe…</li>
            <li>Livraisons&nbsp;: Netflix, Disney+, Apple TV+, Prime Video.</li>
          </ul>
        </div>
        <div class="6u$ 12u$(medium)">
          <h3>Outils & méthodes</h3>
          <ul>
            <li>Chaînes calibrées du nettoyage dialogue au printmaster final.</li>
            <li>Échanges sécurisés, QC détaillé, respect des specs plateformes.</li>
            <li>Monitoring pro, acoustique traitée, jeux de stems prêts à livrer.</li>
            <li>Synergie avec le développement&nbsp;: automatisation des exports et suivi documentaire.</li>
          </ul>
        </div>
      </div>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">Télécharger le CV</a></li>
        <li><a href="mailto:{{ site.email }}" class="button icon fa-calendar">Proposer un projet</a></li>
      </ul>
    </div>
  </section>
</div>
