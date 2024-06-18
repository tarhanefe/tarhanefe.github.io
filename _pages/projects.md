---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<div class="projects-container">
  {% for post in site.projects reversed %}
    <div class="project-box">
      <div class="project-image">
        <img src="{{ post.image }}" alt="{{ post.title }}">
      </div>
      <div class="project-content">
        {% include archive-single.html %}
      </div>
    </div>
  {% endfor %}
</div>

<style>
  .projects-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px; /* Adjust gap between project boxes */
  }
  .project-box {
    width: 300px; /* Adjust width of project boxes */
    max-height: 400px; /* Adjust maximum height of project boxes */
    border: 1px solid #ccc; /* Optional: Add border to project boxes */
    border-radius: 5px; /* Optional: Add border radius to project boxes */
    overflow: hidden; /* Ensure content doesn't overflow the box */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Optional: Add shadow to project boxes */
    display: flex;
    flex-direction: column;
  }
  .project-image img {
    width: 100%; /* Make sure the image covers the full width of the box */
    height: auto; /* Maintain aspect ratio of the image */
  }
  .project-content {
    padding: 15px; /* Add padding inside the project box */
    overflow-y: auto; /* Enable vertical scrolling if content exceeds max height */
  }
</style>
