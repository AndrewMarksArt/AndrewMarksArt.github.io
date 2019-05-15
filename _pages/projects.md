---
title: "Projects"
permalink: /projects/
header:
    image: "/assets/images/lacma_lights.jpg"
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
    {% assign posts = group_items[forloop.index0] %}
    <h2 id="{{ tag | slugify }}" class="archive_subtitle">{{tag}}</h2>
    {% for post in posts %}
        {% include archive-single.html %}
    {% endfor %}
{% endfor %}