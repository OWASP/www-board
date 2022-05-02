---

title: Board
displaytext: Global Board
layout:  null
tab: true
order: 1
tags: board

---

The OWASP Foundation Global Board is comprised of seven elected members who serve for two-year terms. The Call for Global Board nominations occurs in June through August each year, after which OWASP members vote to elect vacancies from qualified nominees during October. Generally our Board meets monthly and meetings are open to the public.

<p class="callout-mono right">Board members are the fiduciaries who steer the organization towards a sustainable future by adopting sound, ethical, and legal governance and financial management policies, as well as by making sure the nonprofit has adequate resources to advance its mission.</p>

(Quoted from National Council of Nonprofits [Board Roles and Responsibilities](https://www.councilofnonprofits.org/tools-resources/board-roles-and-responsibilities))

<section id="board" class="corporate">
<div>	
 {% for member in site.data.members %}
    <div class="member-container">
        <hr/>
        <div class="member-img-container">	
            <div class="member-img" style="background-image: url(https://owasp.org/assets/images/{{ member.image }});"></div>
        </div>
        <div class="member-caption"><h2>{{ member.name }}</h2>
            <hr><strong>{{ member.title }}</strong><br/>
            <div class="member-location">{{member.location}}</div>
            {% if member.twitter %}
            {% assign arr = member.twitter | split: "/" %}
            {% assign lastindex = arr.size | minus: 1 %}
            <div class="member-location"><a href="{{member.twitter}}">@{{ arr[lastindex] }}</a></div>
            {% else %}
            <br/>
            {% endif %}
            {% if member.linkedin %}
            <div class="member-location"><a href="{{member.linkedin}}">{{ member.linkedin }}</a></div>
            {% else %}
            <br/>
            {% endif %}
            <div class="member-info"> Current Term Ends {{ member.term-ends}}.</div>
        </div><br/><br/>
        <div class="member-info">{{ member.description }}</div>
    </div>
{% endfor %}
</div>
</section>
