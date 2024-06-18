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
        {% capture content %}
          {% include archive-single.html %}
        {% endcapture %}
        <div class="content-wrapper">
          {{ content }}
        </div>
        <div class="read-more">
          <em>Read more...</em>
        </div>
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
    max-height: 1000px; /* Set maximum height of project boxes */
    border: 1px solid #ccc; /* Optional: Add border to project boxes */
    border-radius: 5px; /* Optional: Add border radius to project boxes */
    overflow: hidden; /* Ensure content doesn't overflow the box */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Optional: Add shadow to project boxes */
    display: flex;
    flex-direction: column;
    transition: transform 0.3s ease; /* Add transition for zoom effect */
  }
  .project-image img {
    width: 100%; /* Make sure the image covers the full width of the box */
    height: auto; /* Maintain aspect ratio of the image */
  }
  .project-content {
    padding: 15px; /* Add padding inside the project box */
    flex-grow: 1;
    position: relative;
  }
  .content-wrapper {
    max-height: calc(100% - 20px); /* Ensure there's space for "Read more..." */
    overflow: hidden;
  }
  .read-more {
    position: absolute;
    bottom: 15px;
    left: 15px;
    background: white; /* Ensure the text is readable */
    padding: 5px;
  }
  .project-title a:hover {
    color: #3498db; /* Optional: Change color on hover */
  }
  .project-title a:hover ~ .project-box {
    transform: scale(1.05); /* Zoom effect on box when hyperlink is hovered */
  }
</style>
