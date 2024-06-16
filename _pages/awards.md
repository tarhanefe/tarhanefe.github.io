---
layout: archive
title: "Awards"
permalink: /awards/
author_profile: true
---

{% include base_path %}

## Awards

<style>
  .accordion {
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 20px 0;
  }

  .accordion-item {
    border-bottom: 1px solid #ccc;
  }

  .accordion-header {
    cursor: pointer;
    padding: 15px;
    font-size: 16px;
    background-color: #f9f9f9;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .accordion-content {
    display: none;
    padding: 15px;
    background-color: #fff;
  }

  .accordion-content p {
    margin: 0;
  }

  .accordion-icon {
    font-size: 20px;
    transition: transform 0.3s;
  }

  .accordion-item.active .accordion-content {
    display: block;
  }

  .accordion-item.active .accordion-icon {
    transform: rotate(45deg);
  }
</style>

<section id="awards">
  <div class="accordion">
    <div class="accordion-item">
      <h3 class="accordion-header">École Polytechnique Fédérale de Lausanne Excellence Scholarship <span class="accordion-icon">+</span></h3>
      <div class="accordion-content">
        <p>Description of the École Polytechnique Fédérale de Lausanne Excellence Scholarship.</p>
      </div>
    </div>
    <div class="accordion-item">
      <h3 class="accordion-header">TÜBİTAK 2209-B Industry Oriented Projects Support Fund <span class="accordion-icon">+</span></h3>
      <div class="accordion-content">
        <p>Description of the TÜBİTAK 2209-B Industry Oriented Projects Support Fund.</p>
      </div>
    </div>
    <div class="accordion-item">
      <h3 class="accordion-header">Bilkent University Electrical and Electronics Engineering Academical Excellence Award <span class="accordion-icon">+</span></h3>
      <div class="accordion-content">
        <p>Description of the Bilkent University Electrical and Electronics Engineering Academical Excellence Award.</p>
      </div>
    </div>
    <div class="accordion-item">
      <h3 class="accordion-header">Bilkent University High Honor Student <span class="accordion-icon">+</span></h3>
      <div class="accordion-content">
        <p>Description of the Bilkent University High Honor Student.</p>
      </div>
    </div>
    <div class="accordion-item">
      <h3 class="accordion-header">Bilkent University Comprehensive Scholarship <span class="accordion-icon">+</span></h3>
      <div class="accordion-content">
        <p>Description of the Bilkent University Comprehensive Scholarship.</p>
      </div>
    </div>
    <div class="accordion-item">
      <h3 class="accordion-header">Kipaş Science High School Comprehensive Scholarship <span class="accordion-icon">+</span></h3>
      <div class="accordion-content">
        <p>Description of the Kipaş Science High School Comprehensive Scholarship.</p>
      </div>
    </div>
  </div>
</section>

<script>
  document.querySelectorAll('.accordion-header').forEach(header => {
    header.addEventListener('click', () => {
      const item = header.parentElement;
      item.classList.toggle('active');
    });
  });
</script>
