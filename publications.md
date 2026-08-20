---
layout: page
title: Publications
permalink: /publications/
---
# Publications

<div class="page-intro">Selected journal and conference publications. Add or edit entries in <code>_data/publications.yml</code>.</div>

<div class="publication-grid full-list">
{% assign sorted_pubs = site.data.publications | sort: 'year' | reverse %}
{% for pub in sorted_pubs %}
  {% include publication-card.html pub=pub %}
{% endfor %}
</div>
