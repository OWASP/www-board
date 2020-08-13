---
title: OWASP Global Board History
layout: col-sidebar
---

{% assign boardhistory = site.data.board-history | sort: 'year' %}
{% for board in boardhistory %}
### {{ board.year }}
{% for member in board.members %}
* {{ member.name }}{% if member.notes %} (<span style='color:blue;'>{{ member.notes}}</span>){% endif %}
{% endfor %}
{% endfor %}
