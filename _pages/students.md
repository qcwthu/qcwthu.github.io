---
layout: archive
title: "Students"
permalink: /students/
author_profile: true
---

{% assign current_phd_students = site.data.students.current_phd %}
{% assign current_mphil_students = site.data.students.current_mphil %}
{% assign current_research_assistants = site.data.students.current_research_assistants %}
{% assign former_students = site.data.students.former %}

<div class="students-page">

<section class="students-section">
  <h2>Current PhD Students</h2>

{% if current_phd_students and current_phd_students.size > 0 %}
  <ul class="student-list">
{% for student in current_phd_students %}
    <li class="student-list__item">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
      {% assign entry_term = student.term | default: student.period %}
      {% if entry_term %}<span class="student-card__term">({{ entry_term }})</span>{% endif %}
    </li>
{% endfor %}
  </ul>
{% else %}
  <p>The PhD student list is being updated.</p>
{% endif %}

</section>

<section class="students-section">
  <h2>Current MPhil Students</h2>

{% if current_mphil_students and current_mphil_students.size > 0 %}
  <ul class="student-list">
{% for student in current_mphil_students %}
    <li class="student-list__item">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
      {% assign entry_term = student.term | default: student.period %}
      {% if entry_term %}<span class="student-card__term">({{ entry_term }})</span>{% endif %}
    </li>
{% endfor %}
  </ul>
{% else %}
  <p>The MPhil student list is being updated.</p>
{% endif %}

</section>

<section class="students-section">
  <h2>Current Research Assistants</h2>

{% if current_research_assistants and current_research_assistants.size > 0 %}
  <ul class="student-list">
{% for student in current_research_assistants %}
    <li class="student-list__item">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
    </li>
{% endfor %}
  </ul>
{% else %}
  <p>The research assistant list is being updated.</p>
{% endif %}

</section>

<section class="students-section">
  <h2>Previous Members</h2>

{% if former_students and former_students.size > 0 %}
  <ul class="student-list student-list--previous">
{% for student in former_students %}
    <li class="student-list__item">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
      {% assign destination = student.destination | default: student.next %}
      {% if destination %}<span class="student-card__destination">Next: {{ destination }}</span>{% endif %}
    </li>
{% endfor %}
  </ul>
{% else %}
  <p>The previous member list is being updated.</p>
{% endif %}

</section>

</div>
