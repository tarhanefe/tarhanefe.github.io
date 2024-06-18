---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<h1>{{ page.title }}</h1>

<div class="project-list">
  {% for project in site.projects reversed %}
    <div class="project-item">
      <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
      <p>{{ project.excerpt }}</p>
      <a href="{{ project.url | relative_url }}" class="btn btn-primary">Read More</a>
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
    padding: 15px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    width: calc(33.333% - 20px);
    box-sizing: border-box;
  }
  .project-item h2 {
    margin-top: 0;
    font-size: 1.25rem;
  }
  .project-item p {
    font-size: 0.9rem;
    color: #666;
  }
  .btn {
    display: inline-block;
    padding: 8px 12px;
    background: #007bff;
    color: #fff;
    border-radius: 4px;
    text-decoration: none;
  }
  .btn:hover {
    background: #0056b3;
  }
</style>
