---
layout: archive
title: "Students"
permalink: /students/
author_profile: true
---

{% assign current_students = site.data.students.current %}
{% assign former_students = site.data.students.former %}

## Current Students

{% if current_students and current_students.size > 0 %}
{% for student in current_students %}
- {% if student.url %}<a href="{{ student.url }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}{% if student.program %}, {{ student.program }}{% endif %}{% assign entry_term = student.term | default: student.period %}{% if entry_term %}<br>Entry: {{ entry_term }}{% endif %}{% if student.topic %}<br>{{ student.topic }}{% endif %}
{% endfor %}
{% else %}
The student list is being updated.
{% endif %}

## Former Students

{% if former_students and former_students.size > 0 %}
{% for student in former_students %}
- {% if student.url %}<a href="{{ student.url }}" target="_blank" rel="noopener">{{ student.name }}</a>{% else %}{{ student.name }}{% endif %}{% if student.program %}, {{ student.program }}{% endif %}{% assign entry_term = student.term | default: student.period %}{% if entry_term %}<br>Entry: {{ entry_term }}{% endif %}{% assign destination = student.destination | default: student.next %}{% if destination %}<br>Next: {{ destination }}{% endif %}
{% endfor %}
{% else %}
The former student list is being updated.
{% endif %}
