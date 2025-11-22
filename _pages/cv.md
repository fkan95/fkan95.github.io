---
layout: single
title: "CV"
permalink: /cv/
author_profile: false
classes: wide page--cv
---

# Curriculum Vitae

<!-- ======================== EDUCATION ======================== -->

<div class="cv-box">
  <h2>Education</h2>
  {% for item in site.data.cv.education %}
    <div class="cv-entry-grid">

      <!-- Left column: Years -->
      <div class="cv-entry-year">
        {{ item.years }}
      </div>

      <!-- Right column: Details -->
      <div class="cv-entry-details">
        <strong>{{ item.degree }}</strong><br>
        <em>{{ item.institution }}</em>
        {% if item.thesis %}<br><em>Thesis:</em> {{ item.thesis }}{% endif %}
        {% if item.advisor %}<br><em>Advisor:</em> {{ item.advisor }}{% endif %}
        {% if item.comment %}<br>{{ item.comment }}{% endif %}
      </div>

    </div>
  {% endfor %}
</div>


<!-- ======================== POSITIONS ======================== -->

<div class="cv-box">
  <h2>Positions</h2>
  {% for pos in site.data.cv.positions %}
    <div class="cv-entry-grid">

      <div class="cv-entry-year">
        {{ pos.years }}
      </div>

      <div class="cv-entry-details">
        <strong>{{ pos.title }}</strong><br>
        <em>{{ pos.institution }}</em>
        {% if pos.comment %}<br>{{ pos.comment }}{% endif %}
      </div>

    </div>
  {% endfor %}
</div>


<!-- ======================== HONORS ======================== -->

<div class="cv-box">
  <h2>Honors & Awards</h2>
  {% for h in site.data.cv.honors %}
    <div class="cv-entry-grid">

      <div class="cv-entry-year">
        {{ h.year }}
      </div>

      <div class="cv-entry-details">
        <strong>{{ h.title }}</strong><br>
        {{ h.issuer }}
      </div>

    </div>
  {% endfor %}
</div>


<!-- ======================== PUBLICATIONS ======================== -->

<div class="cv-box">
  <h2>Selected Publications</h2>
  {% for pub in site.data.cv.publications %}
    <div class="cv-entry-grid">

      <div class="cv-entry-year">
        {{ pub.year }}
      </div>

      <div class="cv-entry-details">
        {% if pub.url %}
          <a href="{{ pub.url }}">{{ pub.title }}</a>
        {% else %}
          {{ pub.title }}
        {% endif %}
        <br>{{ pub.journal }}
      </div>

    </div>
  {% endfor %}

  <p>Full list on the <a href="/publications/">Publications page</a>.</p>
</div>