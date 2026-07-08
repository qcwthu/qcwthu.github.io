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

## Current PhD Students

{% if current_phd_students and current_phd_students.size > 0 %}
<ul>
{% for student in current_phd_students %}
  <li>{% if student.url %}<a href="{{ student.url }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}{% assign entry_term = student.term | default: student.period %}{% if entry_term %} ({{ entry_term }}){% endif %}</li>
{% endfor %}
</ul>
{% else %}
The PhD student list is being updated.
{% endif %}

## Current MPhil Students

{% if current_mphil_students and current_mphil_students.size > 0 %}
<ul>
{% for student in current_mphil_students %}
  <li>{% if student.url %}<a href="{{ student.url }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}{% assign entry_term = student.term | default: student.period %}{% if entry_term %} ({{ entry_term }}){% endif %}</li>
{% endfor %}
</ul>
{% else %}
The MPhil student list is being updated.
{% endif %}

## Current Research Assistants

{% if current_research_assistants and current_research_assistants.size > 0 %}
<ul>
{% for student in current_research_assistants %}
  <li>{% if student.url %}<a href="{{ student.url }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
The research assistant list is being updated.
{% endif %}

## Previous Members

{% if former_students and former_students.size > 0 %}
<ul>
{% for student in former_students %}
  <li>{% if student.url %}<a href="{{ student.url }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}{% assign destination = student.destination | default: student.next %}{% if destination %}<br>Next: {{ destination }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
The previous member list is being updated.
{% endif %}
