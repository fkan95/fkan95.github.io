---
layout: single
title: "CV"
permalink: /cv/
author_profile: true
---

## Education

{% for item in site.data.cv.education %}
**{{ item.degree }}**, *{{ item.institution }}* — {{ item.years }}  
{% endfor %}

## Positions

{% for pos in site.data.cv.positions %}
**{{ pos.title }}**, *{{ pos.institution }}* — {{ pos.years }}  
{% endfor %}

## Skills

{% for skill in site.data.cv.skills %}
- **{{ skill.name }}**: {{ skill.level }}  
{% endfor %}

## Honors & Awards

{% for h in site.data.cv.honors %}
- **{{ h.title }}**, {{ h.issuer }}, {{ h.year }}  
{% endfor %}

## Selected Publications

{% for pub in site.data.cv.publications %}
- [{{ pub.title }}]({{ pub.url }}) — *{{ pub.journal }}* ({{ pub.year }})  
{% endfor %}

See the full list of publications on my [Publications page](/publications/).