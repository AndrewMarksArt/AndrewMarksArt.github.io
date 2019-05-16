---
layout: archive
permalink: /blog/
title: "Blog"
author_profile: true
header:
    image: "/assets/images/lacma_lights.jpg"
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}