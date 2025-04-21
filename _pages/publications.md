---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

You can find a full list of my papers on my <a href="https://scholar.google.com/citations?user=OwBrmXwAAAAJ">Google Scholar</a>.

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}



