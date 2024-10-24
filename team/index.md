---
title: Team
nav:
  order: 3
  tooltip: About our team
---

<h2><a style="text-decoration: none; color: inherit;margin-top: 5px;">Principal Investigator</a></h2>

{% capture floatcontent %}

<div class="text-center mt-5">
<a style="text-decoration: none; color: inherit;">

  <!-- Avatar -->
  <img src="/images/members_pic/Ling_Website.png"
       style=" max-width: 220px; "
       class="portrait-image"
       />

  <!-- Name & Role -->
  <div class="text-center" style="margin-top: 8px; font-weight: var(--bold); font-size: 1.2rem" > Haonan Ling </div> <br>
<!-- Link to Google Scholar -->
<a href="https://scholar.google.com/citations?hl=en&user=ujiapKkAAAAJ&view_op=list_works&sortby=pubdate" target="_blank">
  <img src="/images/icons/google-scholar.svg" alt="Google Scholar" style="width: 24px; height: 24px; vertical-align: middle; display: inline-block;"/>
</a>&nbsp;&nbsp;&nbsp;

<!-- Link to Email -->
<a href="mailto:haonan.ling@ucf.edu">
  <img src="/images/icons/email.svg" alt="Email" style="width: 24px; height: 24px; vertical-align: middle; display: inline-block;"/>
</a>

{% endcapture %}

{% include float.html content=floatcontent %}

{% assign member = site.members | where: "slug", "Haonan_Ling" | first %}

<p style="margin: 0.1px; font-weight: 450; font-size: 17px; ">  {{ member.position }} </p>
{% for education in member.education %}
<p style="margin: 0.1px; font-size: 17px;">  {{ education }} </p>
{% endfor %}


<a style="text-decoration: none; color: inherit; font-size: 17px;">
Dr. Haonan Ling is an incoming assistant professor in Mechanical and Aerospace Engineering department at UCF starting in Jan 2025. His research interest lies at the intersection of material science, applied physics, and optics and photonics. His PhD dissertation focuses on probing light-matter interactions in nano-structured layered van der Waals materials for advanced nanophotonic applications. He is the recipient of the Dimitris N. Chorafas Foundation Prize (2024) and Dissertation Year Fellowship at UCLA (2023). &nbsp;&nbsp;&nbsp;



<h2><a style="text-decoration: none; color: inherit;">Members</a></h2>


{% capture floatcontent %}                                                                                                        

<div class="text-center mt-5">
<a style="text-decoration: none; color: inherit;">

  <!-- Avatar -->
  <img src="/images/members_pic/knightro.png"
       style=" max-width: 200px; "
       class="portrait-image"
       />

  <!-- Name & Role -->
  <div class="text-center" style="margin-top: 10px; font-weight: var(--bold); font-size: 1.2rem" > Team Openings </div> 
  <div class="text-center" style="margin-top: 10px; font-weight: 400; font-size: 1rem" > Please join us! </div>
{% endcapture %}
{% include float.html content=floatcontent %}
