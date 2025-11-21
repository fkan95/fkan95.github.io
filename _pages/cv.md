---
layout: single
title: "CV"
permalink: /cv/
author_profile: false   # optional: hide sidebar if using full-width CV
---

<div class="cv-box">
  <h2>Education</h2>
  {% for item in site.data.cv.education %}
    <div class="cv-entry">
      <strong>{{ item.degree }}</strong>, *{{ item.institution }}* — {{ item.years }}  
      {% if item.thesis %}<br><em>Thesis:</em> {{ item.thesis }}{% endif %}  
      {% if item.group %}<br><em>Group:</em> {{ item.group }}{% endif %}
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
  <h2>Honors & Awards</h2>
  {% for h in site.data.cv.honors %}
    <div class="cv-entry">
      - **{{ h.title }}**, {{ h.issuer }}, {{ h.year }}
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Publications</h2>
  <p>See my <a href="/publications/">Publications page</a> for the full list.</p>
  See the full list of publications on my [Publications page](/publications/).
</div>
