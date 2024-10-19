---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# Opportunities

 **We are  looking for new PhD students, Postdocs, and Master students to join the team!**

# {% include icon.html icon="fa-solid fa-users" %}Members
We are an interdisciplinary team of researchers passionate about innovative, rigorous, and transparent science. We warmly welcome students and trainees from diverse backgrounds, fostering mutual respect and collaboration. We are committed to fairness and inclusion, ensuring that everyone feels supported and valued.




{% if site.members.team_members.yml %}
  <p>Members collection exists and has {{ site.members.team_members | size }} members.</p>
  <ul>
    {% for member in site.members.team_members %}
      <li>{{ member.name }}</li>
    {% endfor %}
  </ul>
{% else %}
  <p>No members found. The collection may not exist or be empty.</p>
{% endif %}



{% assign number_printed = 0 %}
{% for member in site.members.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div style="display: flex; flex-wrap: wrap; margin-bottom: 20px;">
{% endif %}

<p>Number of team members: {{ site.members.team_members | size }}</p>

<div style="flex: 0 0 50%; padding: 10px;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/members_pic/{{ member.photo }}" style="width: 100%; height: auto; float: left;"/>
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden; list-style-type: none; padding: 0;">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
