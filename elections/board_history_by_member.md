---
title: OWASP Global Board History by Member
layout: col-sidebar
permalink: /board_history/bymember/
---

{% assign board_members = site.data.board-history | sort: 'year' | map: 'members' | map: 'name' | uniq %}
{% assign all_members = '' | split: ',' %}
{% for member in board_members %}
{{ member }}
{% assign years = "" %}
{% for history in site.data.board-history %}
{% for hmember in history.members %}
{% if hmember.name == member %}
{% assign years = years | append: history.year | append: ", " %}
{% endif %}
{% endfor %}
{% endfor %}
{% assign tsize = years.size | minus: 1%}
{{ years | truncate: tsize, " " }}
{% endfor %}

