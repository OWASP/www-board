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

## Board of Directors

The OWASP Foundation Global Board is comprised of seven elected members who serve for two-year terms. The Call for Global Board nominations occurs in June through August each year, after which OWASP members vote to elect vacancies from qualified nominees during October. Generally our Board meets monthly and meetings are open to the public.

<p class="callout-mono right">Board members are the fiduciaries who steer the organization towards a sustainable future by adopting sound, ethical, and legal governance and financial management policies, as well as by making sure the nonprofit has adequate resources to advance its mission.</p>

(Quoted from National Council of Nonprofits [Board Roles and Responsibilities](https://www.councilofnonprofits.org/tools-resources/board-roles-and-responsibilities))

<section id="board" class="corporate">
<div>	
 {% for member in site.data.members %}
    <div class="member-container">
        <div class="member-img-container">	
            <div class="member-img" style="background-image: url(https://owasp.org/assets/images/{{ member.image }});"></div>
        </div>
        <div class="member-caption"><h2>{{ member.name }}</h2>
            <hr><strong>{{ member.title }}</strong><br/>
            <div class="member-location">{{member.location}}</div>
        </div><br/>
        <div class="member-info">{{ member.description }} Current Term Ends {{ member.term-ends}}.</div>
    </div>
    <div style="height:18px;"></div>
{% endfor %}
</div>
</section>

**VOTING FOR 2022 GLOBAL BOARD POSITONS WILL BE COMPLETED IN JANUARY 2022** 2022 Board Officers (Chair, Vice Chair, Secretary, and Treasurer) will elected at the [General Board Meeting on January 25](https://owasp.org/www-board/meetings/202201.html). The 2021 Board officers still hold their office until after the Officer election.

## Board Resources

- [Board Mailing List](https://groups.google.com/a/owasp.org/forum/#!forum/global-board){:target='_blank'}
- [Board Feedback Address - OWASP Members only](mailto:global-board-feedback@owasp.org){:target='_blank'}
- [Action Tracker](https://github.com/OWASP/www-board/projects/1){:target='_blank'}
- [Elections](/www-board/elections/)

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
