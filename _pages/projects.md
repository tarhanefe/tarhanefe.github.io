---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<style>
.project-box {
    border: 2px solid #ccc;
    margin: 10px 0;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-box:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.project-image {
    width: auto;
    height: 200px;
    display: block;
}

.project-content {
    padding: 10px;
}
</style>

{% for post in site.projects reversed %}
  <div class="project-box">
    <div class="project-content">
      {% include archive-single.html %}
    </div>
    <img class="project-image" src="{{ post.image }}" alt="Cover image for {{ post.title }}">
  </div>
{% endfor %}
