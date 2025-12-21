---
layout: page
permalink: /group/
title: group
description: Members of the Madduri Lab at Argonne National Laboratory.
nav: true
nav_order: 3
---

<div class="people">
  {% assign members = site.data.members | sort: "name" %}
  
  <div class="row">
    {% for member in members %}
      <div class="col-sm-6 col-md-4 col-lg-4 mb-4">
        <div class="team-member">
          <div class="profile">
            <img class="img-fluid z-depth-1 rounded" src="{{ member.image }}" alt="{{ member.name }}">
          </div>
          <h4 class="team-name">{{ member.name }}</h4>
          <p class="team-position">{{ member.position }}</p>
          <p class="team-research"><strong>Research:</strong> {{ member.research_interests }}</p>
          {% if member.bio %}
          <p class="team-bio">{{ member.bio }}</p>
          {% endif %}
          {% if member.email %}
          <p class="team-email"><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
          {% endif %}
          {% if member.website %}
          <p class="team-website"><strong>Website:</strong> <a href="{{ member.website }}" target="_blank">{{ member.website }}</a></p>
          {% endif %}
          {% if member.google_scholar %}
          <p class="team-scholar"><strong>Google Scholar:</strong> <a href="{{ member.google_scholar }}" target="_blank">Profile</a></p>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>

<div class="row mt-5">
  <div class="col-sm-12">
    <h3>Join Our Lab</h3>
    <p>We are always looking for talented students, postdocs, and collaborators interested in computational science, AI, and biomedical research. If you're interested in joining our team or collaborating with us, please contact <a href="mailto:rkmadduri@anl.gov">Ravi Madduri</a>.</p>
  </div>
</div>