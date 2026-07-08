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
  <div class="students-section__heading">
    <h2>Current PhD Students</h2>
    <span class="students-section__count">{{ current_phd_students.size }}</span>
  </div>

{% if current_phd_students and current_phd_students.size > 0 %}
  <div class="students-grid">
{% for student in current_phd_students %}
    <article class="student-card">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
      {% assign entry_term = student.term | default: student.period %}
      {% if entry_term %}<span class="student-card__term">{{ entry_term }}</span>{% endif %}
    </article>
{% endfor %}
  </div>
{% else %}
  <p>The PhD student list is being updated.</p>
{% endif %}

</section>

<section class="students-section">
  <div class="students-section__heading">
    <h2>Current MPhil Students</h2>
    <span class="students-section__count">{{ current_mphil_students.size }}</span>
  </div>

{% if current_mphil_students and current_mphil_students.size > 0 %}
  <div class="students-grid">
{% for student in current_mphil_students %}
    <article class="student-card">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
      {% assign entry_term = student.term | default: student.period %}
      {% if entry_term %}<span class="student-card__term">{{ entry_term }}</span>{% endif %}
    </article>
{% endfor %}
  </div>
{% else %}
  <p>The MPhil student list is being updated.</p>
{% endif %}

</section>

<section class="students-section">
  <div class="students-section__heading">
    <h2>Current Research Assistants</h2>
    <span class="students-section__count">{{ current_research_assistants.size }}</span>
  </div>

{% if current_research_assistants and current_research_assistants.size > 0 %}
  <div class="students-grid">
{% for student in current_research_assistants %}
    <article class="student-card">
      <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
    </article>
{% endfor %}
  </div>
{% else %}
  <p>The research assistant list is being updated.</p>
{% endif %}

</section>

<section class="students-section">
  <div class="students-section__heading">
    <h2>Previous Members</h2>
    <span class="students-section__count">{{ former_students.size }}</span>
  </div>

{% if former_students and former_students.size > 0 %}
  <div class="students-grid">
{% for student in former_students %}
    <article class="student-card student-card--previous">
      <span>
        <span class="student-card__name">{% assign homepage = student.url | default: student.homepage %}{% if homepage %}<a href="{{ homepage }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</span>
        {% assign destination = student.destination | default: student.next %}
        {% if destination %}<span class="student-card__destination">Next: {{ destination }}</span>{% endif %}
      </span>
    </article>
{% endfor %}
  </div>
{% else %}
  <p>The previous member list is being updated.</p>
{% endif %}

</section>

</div>
