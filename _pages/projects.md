---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<div class="projects-container">
  {% for project in site.projects reversed %}
    <div class="project-box">
      <a href="{{ project.url | relative_url }}">
        <img src="{{ project.image }}" alt="{{ project.title }}" class="project-image"/>
        <div class="project-content">
          <h3>{{ project.title }}</h3>
          <p>{{ project.excerpt | truncatewords: 30 }}</p>
        </div>
      </a>
    </div>
  {% endfor %}
</div>

<style>
  .projects-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }
  .project-box {
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    width: calc(33.333% - 20px);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s;
  }
  .project-box:hover {
    transform: scale(1.05);
  }
  .project-box a {
    color: inherit;
    text-decoration: none;
  }
  .project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  .project-content {
    padding: 15px;
  }
  @media (max-width: 768px) {
    .project-box {
      width: calc(50% - 20px);
    }
  }
  @media (max-width: 480px) {
    .project-box {
      width: 100%;
    }
  }
</style>
