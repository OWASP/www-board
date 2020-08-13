---
title: Voting
layout:  null
tab: true
order: 2
tags: board
---

## Board Actions

Following is a reverse chronological list of actions with a vote by the Global Board. For additional processing these motions can be accessed in this repo in the _data/votes.yml file. Historically there have been variations in recording votes, which if needed can be retrieved from historical board minutes.

<hr>

<!-- List motions as paragraphs -->
{% for motions in site.data.votes %}
 <p>{{ motions.date }}<br>{{ motions.motion }}. {% if motions.result %}<span style="color:#bb8d04">{{ motions.result }}</span>.{% endif%} {% if motions.vote %} {{ motions.vote }}.{% endif %}</p>
  <hr>
{% endfor %}	
