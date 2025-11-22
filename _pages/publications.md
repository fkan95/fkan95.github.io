{% for pub in site.data.publications_test.test_papers | sort: 'year' | reverse %}
  {{ pub.year }} — {{ pub.title }}<br>
{% endfor %}