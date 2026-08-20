---
layout: page
title: About
permalink: /
description: Xiang Liu, multimodal visual object tracking.
---
<section class="hero-section">
  <div class="hero-copy">
    <p class="eyebrow">
      {{ site.data.profile.name_en }}{% if site.data.profile.name_zh and site.data.profile.name_zh != '' %} / {{ site.data.profile.name_zh }}{% endif %}
    </p>
    <h1 class="hero-title">{{ site.data.profile.positioning_en }}</h1>
    <p class="hero-subtitle">{{ site.data.profile.position_en }}</p>
    <p class="hero-meta">{{ site.data.profile.affiliation_en }}</p>
    <div class="hero-actions">
      {% if site.data.profile.email and site.data.profile.email != '' %}<a class="button-link primary" href="mailto:{{ site.data.profile.email }}">Email</a>{% endif %}
      {% if site.data.profile.scholar and site.data.profile.scholar != '' %}<a class="button-link" href="{{ site.data.profile.scholar }}">Google Scholar</a>{% endif %}
      <a class="button-link" href="https://github.com/{{ site.data.profile.github }}">GitHub</a>
      {% if site.data.profile.orcid and site.data.profile.orcid != '' %}<a class="button-link" href="{{ site.data.profile.orcid }}">ORCID</a>{% endif %}
      <a class="button-link" href="{{ '/cv/' | relative_url }}">CV</a>
    </div>
  </div>
  <div class="hero-portrait">
    {% if site.data.profile.avatar and site.data.profile.avatar != '' %}
      <img src="{{ site.data.profile.avatar | relative_url }}" alt="{{ site.data.profile.name_en }}">
    {% else %}
      <div class="portrait-placeholder">XL</div>
    {% endif %}
  </div>
</section>

## Short Bio

{{ site.data.profile.bio_en }}

## Research Interests

<div class="research-grid">
{% for area in site.data.profile.research_areas_en %}
  <div class="research-card"><strong>{{ area }}</strong></div>
{% endfor %}
</div>

## Selected Publications

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs limit: 5 %}
  {% include publication-card.html pub=pub %}
{% endfor %}
</div>

<p><a class="button-link primary" href="{{ '/publications/' | relative_url }}">More Publications</a></p>

## Recent Updates

<div class="news-timeline">
{% for item in site.data.news limit: 8 %}
  <div class="news-item">
    <span class="news-date">{{ item.date }}</span>
    <span class="news-category">{{ item.category }}</span>
    {% if item.link and item.link != '' %}<a href="{{ item.link }}">{{ item.title }}</a>{% else %}<span>{{ item.title }}</span>{% endif %}
  </div>
{% endfor %}
</div>
