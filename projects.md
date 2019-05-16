---
layout: archive
title: Projects
---

{% for projects in site.projects %}
        <p>{{ projects.content | markdownify }}</p>
{% endfor %}