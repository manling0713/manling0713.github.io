---
layout: page
title: Projects
---

{% assign project_posts = site.posts | where: "categories", "projects" %}

{% for post in project_posts %}
### [{{ post.title }}]({{ post.url }})
{{ post.subtitle }}

**Tags:** {{ post.tags | join: ", " }}

---
{% endfor %}
