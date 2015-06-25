---
layout: page
title: Dashboard || U.S. Open Data
---

# Project Dashboard

{% for project in site.data.dashboard %}
  <div>
    <h2>{{ project.title }}</h2>
    {{ project.description }}
    Status: {{ project.status }}
    Contractor: {{ project.contractor }}
    <a href="{{ project.repository }}">Repository</a>
    <a href="{{ project.blog_entry }}">Blog Entry</a>
    <a href="{{ project.website }}">Website</a>
  </div>
{% endfor %}
