---

layout: col-sidebar
title: Global Board
tags: board

---

<!-- rebuild 3 -->

The OWASP Foundation Global Board is comprised of seven elected members who serve for two-year terms. Each Fall, membership votes to elect new leadership for the Foundation. Generally our Board meets monthly and meetings are open to the public. The Global Board sets the strategic direction of the Foundation, its policies, annual budget, and sets governance and leadership roles. Meetings follow the [Typical Board Meeting Agenda](/www-board/typical_agenda) and are recorded.

Click here for the [OWASP Global Board EU](https://owasp.org/www-board-eu/)


## Upcoming Meetings

{% assign pages = site.pages | sort: 'date' | limit: 12 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'meetings/' %}
 <li>{{ page.date }} - <a href='/www-board{{ page.url }}'>{{ page.title }}</a></li>
 {% endif %}
{% endfor %}
</ul>

## Recent Meetings

{% assign pages = site.pages | order: 'date' | reverse | limit: 6 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'historical/' %}
 <li><a href='/www-board{{ page.url }}'>{{ page.title }}</a></li>
 {% endif %}
{% endfor %}
</ul>

[More Historical Meetings...](/www-board/#div-historical)
