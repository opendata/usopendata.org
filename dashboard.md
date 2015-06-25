---
layout: page
title: Dashboard || U.S. Open Data
---

# Project Dashboard

<ul>
{% for project in site.data.dashboard %}
  <li>
    {{ project.title }}
    {{ project.description }}
    {{ project.status }}
    {{ project.contractor }}
    {{ project.repository }}
    {{ project.blog_entry }}
    {{ project.website }}
  </li>
{% endfor %}
</ul>
