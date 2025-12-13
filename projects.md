---
layout: page
title: Projects
---

{% assign project_posts = site.posts | where: "categories", "projects" %}

{% for post in project_posts %}
<div class="project-item" style="margin-bottom: 2em;">
  
  {% if post.image %}
  <img src="{{ post.image }}" alt="{{ post.title }}" style="max-width:100%; height:auto; margin-bottom:10px;">
  {% endif %}

  ### [{{ post.title }}]({{ post.url }})
  {{ post.subtitle }}

  **Tags:** {{ post.tags | join: ", " }}

  <hr>
</div>
{% endfor %}
