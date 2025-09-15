---
title: Team
nav:
  order: 3
  tooltip: Current and past team members
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
Dr. Haonan Ling is an assistant professor in Mechanical and Aerospace Engineering department at UCF starting in Jan 2025. His research interest lies at the intersection of material science, applied physics, and optics and photonics. His PhD dissertation focuses on probing light-matter interactions in nano-structured layered van der Waals materials for advanced nanophotonic applications. He is the recipient of the Dimitris N. Chorafas Foundation Prize (2024) and Dissertation Year Fellowship at UCLA (2023). &nbsp;&nbsp;&nbsp;



<h2 style="text-align:left !important; text-decoration:none; color:inherit;">Members</h2>
<style>
  /* A left-aligned, wrapping row for cards */
  .members-row{
    display:flex;
    flex-wrap:wrap;
    gap:24px;
    align-items:flex-start;
    justify-content:flex-start; /* left */
  }
  /* Typical card width; adjust to match your theme’s portrait size */
  .members-row > *{
    flex: 0 0 auto; /* don't stretch */
  }
  /* Kill inherited centering from theme classes inside this row */
  .members-row .text-center{ text-align:left; }
</style>

{% comment %}
Capture the include's HTML so we can place it as children of our flex row.
This ensures our custom "Team Openings" card sits in the same row.
{% endcomment %}
{% capture portraits %}
  {% include list.html data="members" component="portrait" filters="role: (phd|undergrad|summer|assistant)" %}
{% endcapture %}

<div class="members-row">
  {{ portraits | strip }}

  <!-- Team Openings card -->
  <div class="text-center" style="width:210px;">
    <a style="text-decoration:none; color:inherit;">
      <img src="/images/members_pic/knightro.png"
           alt="Team Openings"
           class="portrait-image"
           style="max-width:210px; display:block; margin:10px auto 0;" />
      <div style="margin-top:2px; font-weight:var(--bold,700); font-size:1.2rem; text-align:center;">
        <a href="/opportunities" style="text-decoration:none; color:inherit;">
      Team Openings
    </a>
      </div>
      <div style="margin-top:3px; font-weight:400; font-size:1rem; text-align:center;">
        Please join us!
      </div>
    </a>
  </div>
</div>

<h2><a style="text-decoration: none; color: inherit;">Alumni</a></h2>
<p style="font-size: 20px; font-weight: 470; margin-bottom: 1px;">
Undergraduate Research Assistant
</p>
<p style="font-size: 17px; margin-top: 0; display: flex; gap: 40px;">
  <span>Monica Clicquot (Mechanical Engineering)</span>
  <span>01/2025–08/2025</span>
</p>
