---
layout: default
title: Projects
---

{% for projects in site.projects %}


<a href="{{ projects.url | prepend: site.baseurl }}">
        <h2>{{ projects.title }}</h2>
</a>

<p class="post-excerpt">{{ projects.description | truncate: 160 }}</p>

{% endfor %}      