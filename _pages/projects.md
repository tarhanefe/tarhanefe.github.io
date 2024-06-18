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
    padding: 10px;
    margin: 10px 0;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-box:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
</style>

{% for post in site.projects reversed %}
  <div class="project-box">
    {% include archive-single.html %}
  </div>
{% endfor %}
