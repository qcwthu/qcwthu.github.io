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

You can find a full list of my papers on my <a href="https://scholar.google.com/citations?user=OwBrmXwAAAAJ" target="_blank">Google Scholar</a>.

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}


- **A Survey of Frontiers in LLM Reasoning: Inference Scaling, Learning to Reason, and Agentic Systems** <br>
Zixuan Ke, Fangkai Jiao, Yifei Ming, Xuan-Phi Nguyen, Austin Xu, Do Xuan Long, Minzhi Li, **Chengwei Qin**, Peifeng Wang, Silvio Savarese, Caiming Xiong, Shafiq Joty. _Preprint._  
[[Website](https://llm-reasoning-ai.github.io/)][[Paper](https://arxiv.org/abs/2504.09037)]

- **Relevant or Random: Can LLMs Truly Perform Analogical Reasoning?** <br>
**Chengwei Qin**, Wenhan Xia, Tan Wang, Fangkai Jiao, Yuchen Hu, Bosheng Ding, Ruirui Chen, Shafiq Joty. _Preprint._  
[[Paper](https://arxiv.org/abs/2404.12728)]
