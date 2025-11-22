---
layout: single
title: "Publications"
permalink: /publications/
author_profile: false
classes: wide page--cv
---


{% for pub in site.data.publications_test.test_papers | sort: 'year' | reverse %}
  {{ pub.year }} — {{ pub.title }}<br>
{% endfor %}