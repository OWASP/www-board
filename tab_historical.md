---

title: Historical
layout:  null
tab: true
order: 1
tags: board

---

As part of our recent website migration, we have been migrating old Board content to this site. If you're looking for historical agendas or minutes not found below please visit the [Historical Wiki](https://wiki.owasp.org/index.php/Board#tab=Historical_Meeting_Archive).

## Historical Meetings

{% assign pages = site.pages | order: 'date' | reverse | limit: 1000 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'historical/' %}
 <li><a href='/www-board{{ page.url }}'>{{ page.title }}</a></li>
 {% endif %}
{% endfor %}
</ul>

## Minutes
(New and historical ported from wiki.owasp.org)
{% assign pages = site.pages | order: 'date' | reverse | limit: 1000 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'minutes/' %}
 <li><a href='/www-board{{ page.url }}'>{{ page.title }}</a></li>
 {% endif %}
{% endfor %}
</ul>

## Meeting recordings
{% assign recordings = site.static_files | where: "recording", true | reverse | limit: 1000 %}
<ul>
{% for recording in recordings %}
 <li><a href='{{ recording.path }}'>{{ recording.basename }}</a></li>
{% endfor %}
</ul>

## Historical Board Members
Please visit the [Global Board History](/www-board/elections/board_history) for the timeline of board members since 2004 
