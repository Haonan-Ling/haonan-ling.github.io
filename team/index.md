---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# Opportunities
We welcome self-driven and curious young scientists and engineers to join our team and drive advancements in device engineering and material exploration for semiconductor technologies. Our group, along with the schools and departments of University of Central Florida (UCF), offers opportunities for interdisciplinary collaboration to help the next generation researchers grow.

**Prospective PhD students** who are interested in joining my group are welcome to apply to the Mechanical and Aerospace Engineering department at UCF for admission in Fall 2025. Please mention our group when submitting your application materials. 

We are now looking for:
- 1 PhD student to work on 2D materials-based device research and engineering. Past experience in nanofabrication processes, material characterization, nanophotonics and electronics is highly desired but not necessary - a willingness to learn and take action is more important. 
- 1 PhD student to work on optical spectroscopy for material characterization and exploration. Background in optics, spectroscopic and microscopic techniques, applied physics is preferred but not required - what truly matters is a strong desire to learn and take initiative.
<!-- end of the list -->

Motivated Master and undergraduate students, especially in engineering, chemistry, and physics, with a strong interest in learning optics, nanophotonics, spectroscopic techniques, 2D materials, and applied physics are encouraged to apply.

If you are interested in joining our group and would like to chat, please reach out at **haonan.ling@ucf.edu**.

# {% include icon.html icon="fa-solid fa-users" %}Members
We are an interdisciplinary team of researchers passionate about innovative, rigorous, and transparent science. We warmly welcome students and trainees from diverse backgrounds, fostering mutual respect and collaboration. We are committed to fairness and inclusion, ensuring that everyone feels supported and valued.


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
