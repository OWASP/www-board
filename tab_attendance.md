---

title: Attendance
displaytext: Director Attendance
layout:  null
tab: true
order: 4
tags: board

---

The following reflects the board attendance to meetings as a percentage of regular meetings over the calendar year.  Only regular meetings are used in the calculations.  Attendance means that the individual was present for 90% of the meeting.  Missing 10 minutes of a 1.5 hour meeting qualifies as being absent for said meeting.  For more information, refer to the [OWASP Foundation Bylaws](/www-policy/legal/bylaws)

{% assign year = site.time | date: "%Y" %}
{% assign yearly_meetings = site.data.attendance | where: 'year', year %}
{% assign mtg_count = yearly_meetings.size %}
### By Director (over the previous {{mtg_count}} meetings in calendar year {{year}})
{% assign mtg_count = mtg_count | times: 1.0 %}
{% assign directors = site.data.members | sort: 'rank' %}
{% for director in directors %}
{% assign count = 0 %}
{% for mtg in yearly_meetings %}
{% for attendee in mtg.attendees %}
{% if attendee.name == director.name %}
{% assign count = count| plus: 1 %}
{% endif %}
{% endfor %}
{% endfor %}
{% if mtg_count == 0 %}
- {{ director.name }} - No public meetings held as yet
{% else %}
    {% assign mtg_percent = count | divided_by: mtg_count | times: 100 %}
- {{ director.name }} ({{mtg_percent | round: 2}}%)
{% endif %}
{% endfor %}


### By Meeting
{% for mtg in yearly_meetings %}

#### {{mtg.date}}
{% for attendee in mtg.attendees %}
* {{attendee.name}}
{% endfor %}
{% endfor %}