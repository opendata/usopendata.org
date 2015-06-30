---
layout: page
title: Dashboard || U.S. Open Data
---

# Project Dashboard

{% for project in site.data.dashboard %}
  <div class="project">
    <h2>{{ project.title }}</h2>
    <p>{{ project.description }}</p>
    <p>Status: {{ project.status }}</p>
   
    {% if project.contractor == blank %}
    <p>Contractor: {{ project.contractor }}</p>
    {% endif %}
    
    {% if project.repository == blank %}
    <p><a href="{{ project.repository }}">Repository</a>
    {% endif %}
   
    {% if project.blog_entr == blank %}
    | <a href="{{ project.blog_entry }}">Blog Entry</a>
    {% endif %}
   
    {% if project.website == blank %}
    | <a href="{{ project.website }}">Website</a></p>
    {% endif %}
    
  </div>
{% endfor %}
