---
layout: page
title: Projects
full-width: true
---

{% assign project_posts = site.posts | where: "categories", "projects" %}

<div class="row">
{% for post in project_posts %}
  <div class="col-md-4 col-sm-6 mb-4">
    <div class="card h-100 shadow-sm">
      
      {% if post.image %}
      <img class="card-img-top" src="{{ post.image }}" alt="{{ post.title }}" style="height:200px; object-fit:cover;">
      {% endif %}
      
      <div class="card-body">
        <h5 class="card-title"><a href="{{ post.url }}">{{ post.title }}</a></h5>
        <p class="card-text">{{ post.subtitle }}</p>
      </div>
      
      <div class="card-footer">
        <small class="text-muted">Tags: {{ post.tags | join: ", " }}</small>
      </div>

    </div>
  </div>
{% endfor %}
</div>
