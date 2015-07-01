---
layout: page
title: Dashboard || U.S. Open Data
---

# Project Dashboard

<div id="dashboard">

We have projects underway to help to build the capacity of open data. Here is the status of all of our projects.

{% for project in site.data.dashboard %}
  <div class="project">
    <h2>{{ project.title }}</h2>
    <p>{{ project.description }}<br />
    Status: {{ project.status }}<br />
   
    {% if project.contractor != null %}
    Contractor: {{ project.contractor }}<br />
    {% endif %}
    
    <ul>
    {% if project.repository != null %}
    <li><a href="{{ project.repository }}">Repository</a></li>
    {% endif %}
   
    {% if project.blog_entry != null %}
    <li><a href="{{ project.blog_entry }}">Blog Entry</a></li>
    {% endif %}
   
    {% if project.website != null %}
    <li><a href="{{ project.website }}">Website</a></li>
    {% endif %}
    </ul>
    
  </div>
{% endfor %}

</div>
