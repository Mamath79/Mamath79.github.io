---
layout: page
title: Ingénieur du son
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

      <p>
        Ingé son freelance spécialisé en <strong>montage et mixage VF</strong> (doublage), je collabore avec des studios comme
        <a href="https://www.dubbing-brothers.com/#/home" target="_blank" rel="noopener">Dubbing Brothers</a>,
        <a href="https://www.iyuno.com" target="_blank" rel="noopener">Iyuno</a> ou
        <a href="https://www.titrafilm.com" target="_blank" rel="noopener">TitraFilm</a>, et avec des plateformes telles que
        <a href="https://www.netflix.com" target="_blank" rel="noopener">Netflix</a>,
        <a href="https://www.primevideo.com" target="_blank" rel="noopener">Prime Video</a> et
        <a href="https://www.disneyplus.com" target="_blank" rel="noopener">Disney+</a>,
        pour livrer des <strong>masters conformes broadcast/streaming</strong>. Chaîne complète : préparation sessions, nettoyage dialogue,
        design/RX, prémix, mix final, <em>printmaster</em> & livrables. <strong>Workflow remote</strong> disponible (échanges sécurisés, QC).
      </p>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">CV (FR)</a></li>
        <li><a href="mailto:contact@naxencia.fr" class="button icon fa-envelope">Contact</a></li>
      </ul>

      <hr class="major" />

      <h2>Portfolio (sélection)</h2>
      <p class="small">Clique sur une vignette pour afficher les détails.</p>

      <!-- TILES: Cinéma — Enregistrement -->
      <h2>Cinéma — Enregistrement</h2>
      <section class="tiles">
      {% for item in site.data.portfolio_audio.cinema_rec %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic01.jpg') | relative_url }}" alt="{{ item.title }}" />
          </span>
          <a href="#audio-{{ item.slug }}" class="link">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            <p>{{ item.role }}</p>
          </a>
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
      <h2>Cinéma — Mixage</h2>
      <section class="tiles">
      {% for item in site.data.portfolio_audio.cinema_mix %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic03.jpg') | relative_url }}" alt="{{ item.title }}" />
          </span>
          <a href="#audio-{{ item.slug }}" class="link">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            <p>{{ item.role }}</p>
          </a>
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
      <h2>Séries Tv / Tv films</h2>
      <section class="tiles">
      {% for item in site.data.portfolio_audio.series %}
        <article>
          <span class="image">
            <img src="{{ (item.image | default: '/assets/images/pic05.jpg') | relative_url }}" alt="{{ item.title }}" />
          </span>
          <a href="#audio-{{ item.slug }}" class="link">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            <p>{{ item.role }}</p>
          </a>
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
            <li>Montage & mixage VF (doublage), ADR, VO/VM</li>
            <li>Nettoyage dialogue (RX), réduction bruit & clicks</li>
            <li>Conformité loudness (EBU R128/Netflix), stems & PM</li>
            <li>Alignement labial, reconformation, QC technique</li>
            <li>Formats : stéréo, 5.1, M&E, DME</li>
          </ul>
        </div>
        <div class="6u$ 12u$(medium)">
          <h3>Workflow & outils</h3>
          <ul>
            <li>Pro Tools, iZotope RX, Waves, FabFilter</li>
            <li>Échanges sécurisés, livraison cloud, nommage specs</li>
            <li>Monitoring pro, acoustique traitée, ref tracks</li>
            <li>Pipeline remote : validation rapide, itérations cadrées</li>
          </ul>
        </div>
      </div>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">Télécharger le CV</a></li>
        <li><a href="mailto:contact@naxencia.fr" class="button icon fa-calendar">Proposer un projet</a></li>
      </ul>
    </div>
  </section>
</div>
