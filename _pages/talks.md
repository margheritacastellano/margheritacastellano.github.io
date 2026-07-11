---
layout: page
permalink: /talks/
title: Talks
description: Conference presentations, posters, and conferences attended, with slides and posters available for download where provided.
nav: true
nav_order: 4
display_categories:
  - key: Presentation
    label: Presentations
  - key: Poster
    label: Posters
  - key: Attendance
    label: Attendance
---

<div class="talks">

{% for category in page.display_categories %}
<a id="{{ category.key | slugify }}" href=".#{{ category.key | slugify }}">
  <h2 class="category">{{ category.label }}</h2>
</a>
{% assign categorized_talks = site.data.talks.list | where: "type", category.key %}
{% assign sorted_talks = categorized_talks | sort: "date" | reverse %}
{% for talk in sorted_talks %}
<div class="row mt-3 align-items-center">
  <div class="col-sm-8">
    <strong>{{ talk.conference }}</strong>
    <br>
    <span class="text-muted">
      {{ talk.date }}{% if talk.location %}, {{ talk.location }}{% endif %}
    </span>
  </div>
  <div class="col-sm-4 text-sm-end mt-2 mt-sm-0">
    {% if talk.slides %}
      <a href="{{ talk.slides | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Slides</a>
    {% endif %}
    {% if talk.poster %}
      <a href="{{ talk.poster | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Poster</a>
    {% endif %}
  </div>
</div>
<hr>
{% endfor %}
{% endfor %}

</div>
