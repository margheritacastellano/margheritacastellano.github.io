---
layout: page
permalink: /teaching/
title: Teaching
description: Alongside my PhD, I held teaching assistant positions.
nav: true
nav_order: 6
calendar: False
---

<div class="row row-cols-1 mt-3">
{% assign sorted_courses = site.teachings | sort: "year" | reverse %}
{% for course in sorted_courses %}
  <div class="col mb-4">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title">{{ course.title }}</h5>
        <h6 class="card-subtitle mb-2 text-muted">{{ course.year }}</h6>
        <p class="card-text">{{ course.content | strip_html }}</p>
        <p class="card-text"><small class="text-muted">{{ course.location }}</small></p>
      </div>
    </div>
  </div>
{% endfor %}
</div>
