{% for pub in site.data.publications_test.peer_reviewed | sort: 'year' | reverse %}
  {{ pub.year }} — {{ pub.title }}<br>
{% endfor %}