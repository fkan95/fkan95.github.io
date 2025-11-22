---
layout: single
title: "Outreach"
permalink: /outreach/
author_profile: false
classes: wide page--cv
---

<div class="outreach-container">
  {% assign sorted = site.data.outreach | sort: 'date' | reverse %}
  {% assign current_year = "" %}
  {% for item in sorted %}
    {% assign year = item.date | slice: 0,4 %}
    {% if year != current_year %}
      {% unless forloop.first %}</div>{% endunless %}
      <div class="year-group">
        <h2>{{ year }}</h2>
      {% assign current_year = year %}
    {% endif %}

    <div class="outreach-card">
      <h3>{{ item.title }}</h3>
      <p><em>{{ item.type }}</em></p>
      <p>{{ item.description }}</p>
      {% if item.url %}
        <a href="{{ item.url }}" class="button">Learn More</a>
      {% endif %}
    </div>
  {% endfor %}
</div>