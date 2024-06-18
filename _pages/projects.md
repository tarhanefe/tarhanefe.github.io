---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<h1>{{ page.title }}</h1>
<p>Explore a variety of projects showcasing different skills and interests.</p>

<div class="project-list">
  {% for project in site.projects reversed %}
    <a href="{{ project.url | relative_url }}" class="project-link">
      <div class="project-item">
        {% if project.image %}
          <img src="{{ project.image }}" alt="{{ project.title }} image" class="project-image">
        {% endif %}
        <div class="project-content">
          <h3>{{ project.title }}</h3>
          <p>{{ project.excerpt }}</p>
        </div>
      </div>
    </a>
  {% endfor %}
</div>

<style>
  .project-list {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }
  .project-link {
    width: calc(33.333% - 20px);
    text-decoration: none;
    color: inherit;
    transition: transform 0.3s ease;
  }
  .project-link:hover {
    transform: scale(1.05);
  }
  .project-item {
    background: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    display: flex;
    flex-direction: column;
  }
  .project-image {
    width: 100%;
    height: auto;
  }
  .project-content {
    padding: 15px;
  }
  .project-item h3,
  .project-item p {
    text-decoration: none; /* Remove underline from h3 and p elements */
  }
  .project-item h3 {
    margin-top: 0;
    font-size: 1rem;
    color: #333;
  }
  .project-item p {
    font-size: 0.9rem;
    color: #666;
  }
</style>
