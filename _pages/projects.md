---
title: "Projects"
permalink: /projects/
# header:
#   overlay_image: /assets/images/projects.jpg
layout: posts
author_profile: true
---

{% include group-by-array collection=site.projects field="tags" %}

{% for tag in group_names %}
{% assign projects = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in projects %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}