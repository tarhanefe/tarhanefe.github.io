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
      <div class="project-image">
        <img src="{{ post.image }}" alt="{{ post.title }}">
      </div>
      <div class="project-date">
        {{ post.date | date: "%B %d, %Y" }}
      </div>
    </a>
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
    height: 400px; /* Set equal height of project boxes */
    border: 1px solid #ccc; /* Optional: Add border to project boxes */
    border-radius: 5px; /* Optional: Add border radius to project boxes */
    overflow: hidden; /* Ensure content doesn't overflow the box */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Optional: Add shadow to project boxes */
    display: flex;
    flex-direction: column;
    text-decoration: none; /* Remove underline from the link */
    color: inherit; /* Inherit text color */
    transition: transform 0.3s ease; /* Add transition for zoom effect */
  }
  .project-box:hover {
    transform: scale(1.05); /* Zoom effect on box when hovered */
  }
  .project-image img {
    width: 100%; /* Make sure the image covers the full width of the box */
    height: auto; /* Maintain aspect ratio of the image */
    flex-grow: 1; /* Allow image to grow to fill the box */
  }
  .project-date {
    padding: 15px;
    text-align: center;
    background-color: #f9f9f9; /* Optional: Background color for date */
  }
</style>
