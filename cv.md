---
layout: page
title: CV
permalink: /cv/
---
# Curriculum Vitae

<div class="cv-header">
  <div>
    <p class="eyebrow">Academic CV</p>
    <h2>Xiang Liu</h2>
    <p>Ph.D. Candidate · Yunnan University</p>
  </div>
  <a class="button-link primary" href="{{ '/files/Xiang_Liu_CV.pdf' | relative_url }}">PDF CV</a>
</div>

> Replace <code>files/Xiang_Liu_CV.pdf</code> with your real CV PDF. Until then, the PDF button will return 404.

## Research Interests

RGB-T Object Tracking · Multimodal Visual Object Tracking · RGB-Event Tracking · Vision-Language Tracking

## Education

**Ph.D. Candidate**, Yunnan University  
*Add department, degree program, supervisor, and dates here.*

## Publications

{% for pub in site.data.publications %}
- **{{ pub.title }}** — {{ pub.venue }}, {{ pub.year }}.
{% endfor %}

## Academic Service

Add reviewer service, memberships, conference activities, and other professional service here.

## Awards & Honors

Add scholarships, awards, competitions, and honors here.
