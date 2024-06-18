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
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-box:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.project-box img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    opacity: 0.5;
    z-index: -1;
}
</style>

{% for post in site.projects reversed %}
  <div class="project-box">
    <img src="{{ post.image }}" alt="Cover image for {{ post.title }}">
    {% include archive-single.html %}
  </div>
{% endfor %}
