---

layout: col-sidebar
title: Global Board
tags: board

---

<!-- rebuild 6 -->

The OWASP Foundation Global Board is comprised of seven elected members who serve for two-year terms. Each Fall, membership votes to elect new leadership for the Foundation. Generally our Board meets monthly and meetings are open to the public. The Global Board sets the strategic direction of the Foundation, its policies, annual budget, and sets governance and leadership roles. Meetings follow the [Typical Board Meeting Agenda](/typical_agenda) and are recorded.

Click here for the [OWASP Global Board EU](https://owasp.org/www-board-eu/)


## Upcoming Meetings

{% assign pages = site.pages | where_exp: "page", "page.path contains 'meetings/'" | sort: 'date'  %}
<ul>
{% for page in pages %}
 <li>{{ page.date }} - <a href='/{{ page.url }}'>{{ page.title }}</a></li> 
 {% if forloop.index > 11%}
  {%break%}
 {%endif%}
{% endfor %}
</ul>

## Recent Meetings

{% assign pages = site.pages | where_exp: "page", "page.path contains 'meetings-historical'" | order: 'date' | reverse %}
<ul>
{% for page in pages %}
 <li><a href='/{{ page.url }}'>{{ page.title }}</a></li>
 {% if forloop.index > 5 %}
 {%break%}
 {%endif%}
{% endfor %}
</ul>

<a href="javascript: t = Date.now(); location.assign('/?v=' + t + '#div-historical');">More Historical Meetings</a>
