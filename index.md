---

layout: col-sidebar
title: Global Board
tags: board

---

<!-- rebuild 3 -->

The OWASP Foundation Global Board is comprised of seven elected members who serve for two-year terms. Each Fall, membership votes to elect new leadership for the Foundation. Generally our Board meets monthly and meetings are open to the public. The Global Board sets the strategic direction of the Foundation, its policies, annual budget, and sets governance and leadership roles. Meetings follow the [Typical Board Meeting Agenda](/www-board/typical_agenda) and are recorded. 

## Upcoming Meetings
{% assign pages = site.pages | sort: 'date' | limit: 12 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'meetings/' %}
 <li>{{ page.date }} - <a href='/www-board{{ page.url }}'>{{ page.title }}</a></li>
 {% endif %}
{% endfor %}
</ul>

## Board Resources
- [Board Mailing List](https://groups.google.com/a/owasp.org/forum/#!forum/global-board){:target='_blank'}
- [Board Feedback Address - OWASP Members only](mailto:global-board-feedback@owasp.org){:target='_blank'}
- [Action Tracker](https://github.com/OWASP/www-board/projects/1){:target='_blank'}
- [Elections](/www-board/elections/){:target='_blank'}

## Current Membership

* [Sherif Mansour](mailto:sherif.mansour@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'{:target='_blank'}, Chair
* [Vandana Verma Sehgal](mailto:Vandana.verma@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'}, Vice Chair
* [Bil Corry](mailto:bil.corry@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'}, Secretary
* [Grant Ongers](mailto:grant.ongers@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'}, Treasurer
* [Joubin Jabbari](mailto:joubin.jabbari@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'}
* [Martin Knobloch](mailto:martin.knobloch@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'}
* [Owen Pendlebury](mailto:owen.pendlebury@owasp.org?subject=OWASP%20Global%20Board){:target='_blank'}

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


