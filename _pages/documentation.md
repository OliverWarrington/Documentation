---
layout: archive
title: "Documentation"
permalink: /docs/
author_profile: false
---

{% include group-by-array collection=site.documentation field="categories" %}
{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
