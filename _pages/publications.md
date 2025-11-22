---
layout: single
title: "Publications"
permalink: /publications/
author_profile: false
classes: wide page--cv
---

<div class="cv-box">
  <h2>Peer-reviewed Articles</h2>
  {% for pub in site.data.publications.peer_reviewed %}
    <div class="cv-entry cv-2col">
      <div class="cv-left">{{ pub.year }}</div>
      <div class="cv-right">
        {% if pub.url %}
          <a href="{{ pub.url }}"><strong>{{ pub.title }}</strong></a>
        {% else %}
          <strong>{{ pub.title }}</strong>
        {% endif %}
        <br>
        <em>{{ pub.authors }}</em><br>
        {{ pub.journal }}
      </div>
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Preprints</h2>
  {% for pub in site.data.publications.preprints %}
    <div class="cv-entry cv-2col">
      <div class="cv-left">{{ pub.year }}</div>
      <div class="cv-right">
        {% if pub.url %}
          <a href="{{ pub.url }}"><strong>{{ pub.title }}</strong></a>
        {% else %}
          <strong>{{ pub.title }}</strong>
        {% endif %}
        <br>
        <em>{{ pub.authors }}</em><br>
        arXiv: {{ pub.arxiv }}
      </div>
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Talks</h2>
  {% for talk in site.data.publications.talks %}
    <div class="cv-entry cv-2col">
      <div class="cv-left">{{ talk.year }}</div>
      <div class="cv-right">
        <strong>{{ talk.title }}</strong><br>
        {{ talk.event }}, {{ talk.location }}
      </div>
    </div>
  {% endfor %}
</div>