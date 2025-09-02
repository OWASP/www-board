- [Global Board Main Page](/)
- [Global Board Elections](/elections/)
- [Global Board History](/board_history)

### Upcoming Meetings
The OWASP Global Board typically meets over video-conference on the third Tuesday of each month. 

{% assign pages = site.pages | order: 'date' | limit: 6 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'meetings/' %}
 <li><a href='https://board.owasp.org{{ page.url }}'>{{ page.title }}</a></li>
 {% endif %}
{% endfor %}
</ul>
