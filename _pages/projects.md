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
  {% for post in site.projects reversed %}
    <a href="{{ post.url | relative_url }}" class="project-link">
      <div class="project-item">
        {% if post.header.teaser %}
          <img src="{{ post.header.teaser | prepend: site.baseurl }}" alt="{{ post.title }} image" class="project-image">
        {% endif %}
        <div class="project-content">
          <h3>{{ post.title }}</h3>
          <p>{{ post.excerpt }}</p>
        </div>
        <div class="project-footer">
          <p><i class="fa fa-fw fa-calendar" aria-hidden="true"></i> <time datetime="{{ post.date | default: "1900-01-01" | date_to_xmlschema }}">{{ post.date | default: "1900-01-01" | date: "%B %d, %Y" }}</time></p>
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
    height: 420px; /* Adjusted height to accommodate footer */
    box-sizing: border-box;
    transition: transform 0.3s ease;
  }
  .project-image {
    width: 100%;
    height: 150px; /* Fixed height for images */
    object-fit: cover;
  }
  .project-content {
    padding: 15px;
    flex-grow: 1;
  }
  .project-footer {
    padding: 10px 15px;
    background-color: #f1f1f1;
    text-align: right;
  }
  .project-item h3, .project-item p {
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
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 5; /* Limit to 5 lines */
    -webkit-box-orient: vertical;
  }
  .project-footer p {
    margin: 0;
    font-size: 0.8rem;
    color: #888;
  }
</style>
