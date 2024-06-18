---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<style>
.project-box {
    position: relative;
    border: 2px solid #ccc;
    padding: 10px;
    margin: 10px 0;
    overflow: hidden;
    background-size: cover;
    background-position: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-box:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.project-content {
    position: relative;
    z-index: 1;
}

.project-box::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(255, 255, 255, 0.5); /* Adjust the transparency as needed */
    z-index: 0;
}
</style>

{% for post in site.projects reversed %}
  <div class="project-box" style="background-image: url('{{ post.image }}');">
    <div class="project-content">
      {% include archive-single.html %}
    </div>
  </div>
{% endfor %}
