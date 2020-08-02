---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

All papers have been subject to peer review unless indicated otherwise. *indicates equal contributions.

Click on a paper to view its short summary.

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

