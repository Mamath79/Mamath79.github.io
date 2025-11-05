---
layout: page
lang: en
translation_key: audio
title: Sound Engineer Portfolio
description: Recording, editing, and mixing for film and TV dubbing. 20 years of experience in studios and remote workflows.
image: assets/images/DSC00243-small-34.jpg
banner_no_overlay: false
banner_fit: contain
nav-menu: true
show_tile: true
tile_order: 2
permalink: /en/audio/
---

<!-- Main -->
<div id="main" class="alt">
  <section id="one">
    <div class="inner">
      <header class="major">
      </header>

      <div class="box audio-summary">
        <p><strong>20+ years</strong> in sound engineering | French ADR, editing & mixing | Secure remote workflows.</p>
        <p><strong>Studios:</strong> Dubbing Brothers, Iyuno, TitraFilm | <strong>Platforms:</strong> Netflix, Disney+, Apple TV+, Prime Video.</p>
      </div>

      <nav class="audio-toc">
        <ul>
          <li><a href="#audio-cinema-rec">Cinema — Recording</a></li>
          <li><a href="#audio-cinema-mix">Cinema — Mixing</a></li>
          <li><a href="#audio-series">TV series / TV movies</a></li>
        </ul>
      </nav>

      <p>
        I have been a sound engineer for over two decades, supporting feature films, series, and documentaries in leading Parisian studios.
      </p>
      <p>
        I handle recording, dialogue editing, and mixing with a blend of precision and creative direction.
      </p>
      <p>
        My post-production dialogue expertise pairs naturally with software development: workflow automation, streamlined processes, and uncompromising quality.
      </p>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">Résumé (FR)</a></li>
        <li><a href="mailto:{{ site.email }}" class="button icon fa-paper-plane">Start a project</a></li>
      </ul>

      <hr class="major" />

      <h2>Portfolio (selection)</h2>
      <p class="small">A few highlights where technical precision meets artistic direction.</p>
      <p class="small">Click a tile to display the details.</p>

      <!-- TILES: Cinema — Recording -->
      <h2 id="audio-cinema-rec">Cinema — Recording</h2>
      <section class="tiles tiles--contain">
      {% for item in site.data.portfolio_audio_en.cinema_rec %}
        <article>
          <span class="image">
            <img src="{{ item.image | default: '/assets/images/pic01.jpg' | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Audio project' }}" loading="lazy" decoding="async" />
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
          </header>
          <a href="#audio-{{ item.slug }}" class="link primary" aria-label="View {{ item.title }}"></a>
        </article>
        <div id="audio-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Close"></a>
          <div class="modal-content" style="background-image: url('{{ item.image | default: '/assets/images/pic01.jpg' | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Close">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client or item.doubleur %}
              <p>
                On this project I handled
                {% if item.role %}{{ item.role | downcase }}{% else %}my scope{% endif %}
                {% if item.doubleur %}
                  at <a href="{{ item.doubleur }}" target="_blank" rel="noopener">
                    {{ item.doubleur | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}
                {% if item.client %}
                  for <a href="{{ item.client }}" target="_blank" rel="noopener">
                    {{ item.client | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}.
              </p>
              {% endif %}
              <div class="actions">
                {% if item.link %}<a class="button" href="{{ item.link }}" target="_blank" rel="noopener">See the release</a>{% endif %}
                <a class="button alt" href="#close">Close</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <!-- TILES: Cinema — Mixing -->
      <h2 id="audio-cinema-mix">Cinema — Mixing</h2>
      <section class="tiles tiles--contain">
      {% for item in site.data.portfolio_audio_en.cinema_mix %}
        <article>
          <span class="image">
            <img src="{{ item.image | default: '/assets/images/pic01.jpg' | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Audio project' }}" loading="lazy" decoding="async" />
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
          </header>
          <a href="#audio-{{ item.slug }}" class="link primary" aria-label="View {{ item.title }}"></a>
        </article>
        <div id="audio-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Close"></a>
          <div class="modal-content" style="background-image: url('{{ item.image | default: '/assets/images/pic01.jpg' | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Close">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client or item.doubleur %}
              <p>
                On this project I handled
                {% if item.role %}{{ item.role | downcase }}{% else %}my scope{% endif %}
                {% if item.doubleur %}
                  at <a href="{{ item.doubleur }}" target="_blank" rel="noopener">
                    {{ item.doubleur | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}
                {% if item.client %}
                  for <a href="{{ item.client }}" target="_blank" rel="noopener">
                    {{ item.client | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}.
              </p>
              {% endif %}
              <div class="actions">
                {% if item.link %}<a class="button" href="{{ item.link }}" target="_blank" rel="noopener">See the release</a>{% endif %}
                <a class="button alt" href="#close">Close</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <!-- TILES: Series -->
      <h2 id="audio-series">TV series / TV movies</h2>
      <section class="tiles tiles--contain">
      {% for item in site.data.portfolio_audio_en.series %}
        <article>
          <span class="image">
            <img src="{{ item.image | default: '/assets/images/pic01.jpg' | relative_url }}" alt="{{ item.title }} — {{ item.role | default: 'Audio project' }}" loading="lazy" decoding="async" />
          </span>
          <header class="major">
            <h3>{{ item.title }}</h3>
            {% if item.client %}<p><strong>Client:</strong> {{ item.client }}</p>{% endif %}
            {% if item.role %}<p>{{ item.role }}</p>{% endif %}
          </header>
          <a href="#audio-{{ item.slug }}" class="link primary" aria-label="View {{ item.title }}"></a>
        </article>
        <div id="audio-{{ item.slug }}" class="modal">
          <a href="#close" class="modal-overlay" aria-label="Close"></a>
          <div class="modal-content" style="background-image: url('{{ item.image | default: '/assets/images/pic01.jpg' | relative_url }}');">
            <a href="#close" class="modal-close" aria-label="Close">&times;</a>
            <div class="shade"></div>
            <div class="modal-body">
              <h3>{{ item.title }}</h3>
              {% if item.client or item.doubleur %}
              <p>
                On this project I handled
                {% if item.role %}{{ item.role | downcase }}{% else %}my scope{% endif %}
                {% if item.doubleur %}
                  at <a href="{{ item.doubleur }}" target="_blank" rel="noopener">
                    {{ item.doubleur | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}
                {% if item.client %}
                  for <a href="{{ item.client }}" target="_blank" rel="noopener">
                    {{ item.client | replace: 'https://','' | replace:'http://','' | replace:'www.','' | split: '/' | first }}
                  </a>
                {% endif %}.
              </p>
              {% endif %}
              <div class="actions">
                {% if item.link %}<a class="button" href="{{ item.link }}" target="_blank" rel="noopener">See the release</a>{% endif %}
                <a class="button alt" href="#close">Close</a>
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </section>

      <hr class="major" />

      <div class="row">
        <div class="6u 12u$(medium)">
          <h3>Key skills</h3>
          <ul>
            <li>Editing & mixing: Pro Tools, ADR, VO, FX, music.</li>
            <li>Workflow & automation: templates, macros, tailored scripts.</li>
            <li>Studios & clients: Dubbing Brothers, TitraFilm, Iyuno, Deluxe…</li>
            <li>Deliveries: Netflix, Disney+, Apple TV+, Prime Video.</li>
          </ul>
        </div>
        <div class="6u$ 12u$(medium)">
          <h3>Tools & methods</h3>
          <ul>
            <li>Calibrated chains from dialogue clean-up to final printmaster.</li>
            <li>Secure file exchange, detailed QC, compliance with platform specs.</li>
            <li>Pro monitoring, treated acoustics, delivery-ready stems.</li>
            <li>Synergy with development: automated exports and documentation flow.</li>
          </ul>
        </div>
      </div>

      <ul class="actions">
        <li><a href="{{ '/assets/cv/CV-2025-FR-V6_compressed.pdf' | relative_url }}" class="button special icon fa-download">Download résumé (FR)</a></li>
        <li><a href="mailto:{{ site.email }}" class="button icon fa-calendar">Suggest a project</a></li>
      </ul>
    </div>
  </section>
</div>
