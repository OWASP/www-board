---

title: Voting
layout: col-generic

---



{% capture motion_dates %}{% for vote in site.data.votes %}{{ vote.date }}{% if forloop.last == false %}::{% endif%}{% endfor %}{% endcapture %}
{% assign date_array = motion_dates | split: '::' | uniq %}
{% for vdate in date_array %}
<hr>
{{ vdate | strip }}<br>
{% for vote in site.data.votes %}
{% if vdate contains vote.date %}
<strong>motion</strong>: {{vote.motion}}<br>
<strong>result</strong>: {{vote.result}}<br>{% if vote.vote %}<strong>vote</strong>: {{vote.vote}}<br>{% endif %}
<p>
{% endif %}
{% endfor %}
{% endfor %}