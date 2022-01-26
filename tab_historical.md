---

title: Historical
displaytext: Past Meetings
layout:  null
tab: true
order: 2
tags: board

---

As part of our recent website migration, we have been migrating old Board content to this site. If you're looking for historical agendas or minutes not found below please visit the [Historical Wiki](https://wiki.owasp.org/index.php/Board#tab=Historical_Meeting_Archive).

## Past Meetings

{% assign pages = site.pages | order: 'date' | reverse | limit: 1000 %}
<ul>
{% for page in pages %}
 {% if page.path contains 'historical/' %}
 <li>{{page.date}}-<a href='/www-board{{ page.url }}'>{{ page.title }}</a></li>
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

See meeting minutes for the recordings

## Historical meetings prior to 2021

### 2020 

* [December 2020](https://drive.google.com/file/d/1fzlUy82xn1pz-QzO_aeV8gn-OMR4EUpj/view?usp=sharing){:target='_blank'}
* [November 2020](https://drive.google.com/file/d/1q7JzUJE3zNPP6WzRwex2kB5CxJfsU3Rh/view?usp=sharing){:target='_blank'}
* [November 2020 - Special Events Meeting 2020](https://drive.google.com/file/d/1-2CoQBvqG8vtnmTiuwzcsffCJq62Bi3s/view?usp=sharing){:target='_blank'}
* [October 2020](https://drive.google.com/file/d/1xa5uJRchRsr6RJ1b-bWRpcQu3Jel1Lve/view?usp=sharing){:target='_blank'}
* [September 2020](https://drive.google.com/file/d/1VfevWytCRsr9-0vKzD9JuCqky2Zmi3QM/view?usp=sharing){:target='_blank'}
* [August 2020](https://drive.google.com/file/d/1GE0WTtnmTqzDiYTbRq2-w6jfcvEEe6GA/view?usp=sharing){:target='_blank'}
* [August 2020 - Special Meeting](https://drive.google.com/file/d/1-CbNlgDtgx5D38zD9qx7M8NlT5FwUGyz/view?usp=sharing){:target='_blank'}
* [July 2020](https://drive.google.com/file/d/1u_6wbjyBtRcmkSl_uuUAZZcRbY1bC9N7/view?usp=sharing){:target='_blank'}
* [June 2020](https://drive.google.com/file/d/1G6L1FR5KktWfKVY1ebsVeov2AAWnrkpk/view?usp=sharing){:target='_blank'}
* [May 2020](https://drive.google.com/file/d/1G6yn2tP8odxVEd3oGUeUb6e4yfJj_VeU/view?usp=sharing){:target='_blank'}
* [April 2020](https://drive.google.com/file/d/1GAeGM247FjiEMahhBJPd8SVwxYbi9qTB/view?usp=sharing){:target='_blank'}
* [February 2020](https://drive.google.com/file/d/1GCkopvPUONSybj7EobrUNP4rWINiNzre/view?usp=sharing){:target='_blank'}
* [January 2020](https://drive.google.com/file/d/1GDjvk9n8Z7FhD4cfS_L_z85ctUEh0r6V/view?usp=sharing){:target='_blank'}

### 2019

* [November 2019](https://drive.google.com/file/d/1G3IiggueKUSCIls-ARZGcGYOiBnc4Frz/view?usp=sharing){:target='_blank'} - Audio

## Historical Board Members

Please visit the [Global Board History](/www-board/elections/board_history) for the timeline of board members since 2004 
