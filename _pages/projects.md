---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<div class="projects-container">
  {% for post in site.projects reversed %}
    <a class="project-box" href="{{ post.url }}">
      {% include archive-single.html %}
    </a>
  {% endfor %}
</div>

<style>
  .projects-container {
    display: flex;
    flex-direction: column;
    gap: 20px; /* Adjust gap between project boxes */
  }
  .project-box {
    display: block; /* Make the entire box a clickable link */
    border: 1px solid #ccc; /* Optional: Add border to project boxes */
    border-radius: 5px; /* Optional: Add border radius to project boxes */
    overflow: hidden; /* Ensure content doesn't overflow the box */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Optional: Add shadow to project boxes */
    text-decoration: none; /* Remove underline from the link */
    color: inherit; /* Inherit text color */
    padding: 15px; /* Add padding inside the project box */
    transition: transform 0.3s ease; /* Add transition for zoom effect */
  }
  .project-box:hover {
    transform: scale(1.05); /* Zoom effect on box when hovered */
  }
</style>
