---
layout: single
title: "CV"
permalink: /cv/
author_profile: false   # optional: hide sidebar for full-width CV
---

# Curriculum Vitae

<div class="cv-box">
  <h2>Education</h2>
  {% for item in site.data.cv.education %}
    <div class="cv-entry">
      <strong>{{ item.degree }}</strong>, *{{ item.institution }}* — {{ item.years }}
      {% if item.thesis %}<br><em>Thesis:</em> {{ item.thesis }}{% endif %}
      {% if item.advisor %}<br><em>Advisor:</em> {{ item.advisor }}{% endif %}
      {% if item.comment %}<br><em>Comment:</em> {{ item.comment }}{% endif %}
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Positions</h2>
  {% for pos in site.data.cv.positions %}
    <div class="cv-entry">
      <strong>{{ pos.title }}</strong>, *{{ pos.institution }}* — {{ pos.years }}
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Skills</h2>
  {% for skill in site.data.cv.skills %}
    <div class="cv-entry">
      - <strong>{{ skill.name }}</strong>: {{ skill.level }}
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Honors & Awards</h2>
  {% for h in site.data.cv.honors %}
    <div class="cv-entry">
      - <strong>{{ h.title }}</strong>, {{ h.issuer }}, {{ h.year }}
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Publications</h2>
  {% for pub in site.data.cv.publications %}
    <div class="cv-entry">
      {% if pub.url %}
        <a href="{{ pub.url }}">{{ pub.title }}</a>
      {% else %}
        {{ pub.title }}
      {% endif %}
      , {{ pub.journal }}, {{ pub.year }}
    </div>
  {% endfor %}
  <p>See the full list of publications on my <a href="/publications/">Publications page</a>.</p>
</div>