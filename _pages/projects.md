---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}


<div class="project-list">
  {% for project in site.projects reversed %}
    <div class="project-item">
      <a href="{{ project.url | relative_url }}" class="project-link">
        {% if project.image %}
          <img src="{{ project.image }}" alt="{{ project.title }} image" class="project-image">
        {% endif %}
        <div class="project-content">
          <h3>{{ project.title }}</h3>
          <p>{{ project.excerpt }}</p>
        </div>
      </a>
    </div>
  {% endfor %}
</div>

<style>
  .project-list {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
  }
  .project-item {
    background: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    width: calc(33.333% - 20px);
    box-sizing: border-box;
    overflow: hidden;
  }
  .project-link {
    color: inherit;
    text-decoration: none;
    display: block;
  }
  .project-image {
    width: 100%;
    height: auto;
  }
  .project-content {
    padding: 15px;
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
