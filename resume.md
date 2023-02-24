---
title: 'Moje resume'
layout: page
---



{% comment %}
  Resume content starts here
{% endcomment %}

<div class="resume-section">
  <h2>{{ data.resume.basics.name }}</h2>
  <p class="resume-label">{{ data.resume.basics.label }}</p>
  {% if data.resume.basics.image %}
    <img src="{{ data.resume.basics.image }}" alt="{{ data.resume.basics.name }}" class="resume-image">
  {% endif %}
  <p>{{ data.resume.basics.summary }}</p>
  <ul class="resume-contact">
    {% if data.resume.basics.email %}
      <li><a href="mailto:{{ data.resume.basics.email }}"><i class="fa fa-envelope"></i> {{ data.resume.basics.email }}</a></li>
    {% endif %}
    {% if data.resume.basics.phone %}
      <li><a href="tel:{{ data.resume.basics.phone }}"><i class="fa fa-phone"></i> {{ data.resume.basics.phone }}</a></li>
    {% endif %}
    {% if data.resume.basics.website %}
      <li><a href="{{ data.resume.basics.website }}" target="_blank"><i class="fa fa-globe"></i> {{ data.resume.basics.website }}</a></li>
    {% endif %}
    {% if data.resume.basics.profiles %}
      {% for profile in data.resume.basics.profiles %}
        <li><a href="{{ profile.url }}" target="_blank"><i class="fa fa-{{ profile.network | downcase }}"></i> {{ profile.username }}</a></li>
      {% endfor %}
    {% endif %}
  </ul>
</div>

{% if data.resume.work %}
<div class="resume-section">
  <h2>Work Experience</h2>
  {% for job in data.resume.work %}
    <div class="resume-entry">
      <h3>{{ job.position }}</h3>
      <h4>{{ job.company }}</h4>
      {% if job.startDate %}
        <p class="resume-date">{{ job.startDate | date: "%b %Y" }} - {% if job.endDate %}{{ job.endDate | date: "%b %Y" }}{% else %}Present{% endif %}</p>
      {% endif %}
      {% if job.location %}
        <p class="resume-location">{{ job.location.city }}, {{ job.location.countryCode }}</p>
      {% endif %}
      {% if job.website %}
        <p><a href="{{ job.website }}" target="_blank">{{ job.website }}</a></p>
      {% endif %}
      {% if job.summary %}
        <p>{{ job.summary }}</p>
      {% endif %}
      {% if job.highlights %}
        <ul>
          {% for highlight in job.highlights %}
            <li>{{ highlight }}</li>
          {% endfor %}
        </ul>
      {% endif %}
    </div>
  {% endfor %}
</div>
{% endif %}

<div class="resume-section">
  <h2>Volunteer Experience</h2>
  {% for volunteer in data.resume.volunteer %}
    <div class="resume-entry">
      <h3>{{ volunteer.position }}</h3>
      <h4>{{ volunteer.organisation }}</h4>
      {% if volunteer.startDate %}
        <p class="resume-date">{{ volunteer.startDate | date: "%b %Y" }} - {% if volunteer.endDate %}{{ volunteer.endDate | date: "%b %Y" }}{% else %}obecnie{% endif %}</p>
      {% endif %}
      {% if volunteer.website %}
        <p><a href="{{ volunteer.website }}" target="_blank">{{ volunteer.website }}</a
{% endif %}
{% endfor %}