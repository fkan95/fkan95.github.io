---
layout: single
title: "Publications"
permalink: /publications/
author_profile: false
classes: wide page--cv
---

{% assign sections = 
  "peer_reviewed,Preprints,preprints,theses,Theses,talks,Talks" | split: "," %}

<!-- Helper: convert year/range to number for sorting -->
{% capture year_num %}
  {% raw %}
  {% assign y = pub.year | split: "-" | first | strip %}
  {% assign y_num = y | plus: 0 %}
  {% endraw %}
{% endcapture %}

<div class="cv-box">
  <h2>Peer-reviewed Articles</h2>
  {% assign pubs = site.data.publications.peer_reviewed %}
  {% assign pubs_sorted = pubs | sort: "year" | reverse %}
  {% for pub in pubs_sorted %}
    {% assign start_year = pub.year | split: "-" | first | strip | plus: 0 %}
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
  <p><em>* Joint first authorship.</em></p>
</div>

<div class="cv-box">
  <h2>Preprints</h2>
  {% assign pubs = site.data.publications.preprints %}
  {% assign pubs_sorted = pubs | sort: "year" | reverse %}
  {% for pub in pubs_sorted %}
    {% assign start_year = pub.year | split: "-" | first | strip | plus: 0 %}
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
  <h2>Theses</h2>
  {% assign pubs = site.data.publications.theses %}
  {% assign pubs_sorted = pubs | sort: "year" | reverse %}
  {% for pub in pubs_sorted %}
    {% assign start_year = pub.year | split: "-" | first | strip | plus: 0 %}
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
      </div>
    </div>
  {% endfor %}
</div>

<div class="cv-box">
  <h2>Talks</h2>
  {% assign pubs = site.data.publications.talks %}
  {% assign pubs_sorted = pubs | sort: "year" | reverse %}
  {% for talk in pubs_sorted %}
    {% assign start_year = talk.year | split: "-" | first | strip | plus: 0 %}
    <div class="cv-entry cv-2col">
      <div class="cv-left">{{ talk.year }}</div>
      <div class="cv-right">
        <strong>{{ talk.title }}</strong><br>
        {{ talk.event }}, {{ talk.location }}
      </div>
    </div>
  {% endfor %}
</div>