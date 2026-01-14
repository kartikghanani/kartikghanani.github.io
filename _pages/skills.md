---
title: "Skills"
permalink: /skills/
layout: single
classes: wide
---

<div class="skills-wrap">
  <h1 class="skills-title">Skills and Technologies</h1>

  <div class="skills-card">
    <div class="skills-card__head">
      <div>
        <h2>Daily Stack</h2>
        <p>Tools, resources, and technologies I use daily</p>
      </div>
    </div>

    <div class="skills-grid">
      {% for s in site.data.skills.daily %}
      <div class="skill-item">
        <div class="skill-icon">
          <img src="{{ s.icon }}" alt="{{ s.name }} logo" loading="lazy">
        </div>
        <div class="skill-text">
          <div class="skill-name">{{ s.name }}</div>
          <div class="skill-sub">{{ s.note }}</div>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>

  <div class="skills-card" style="margin-top: 18px;">
    <div class="skills-card__head">
      <div>
        <h2>Other Technologies</h2>
        <p>Tools, resources, and technologies I have used in the past</p>
      </div>
    </div>

    <div class="skills-grid">
      {% for s in site.data.skills.other %}
      <div class="skill-item">
        <div class="skill-icon">
          <img src="{{ s.icon }}" alt="{{ s.name }} logo" loading="lazy">
        </div>
        <div class="skill-text">
          <div class="skill-name">{{ s.name }}</div>
          <div class="skill-sub">{{ s.note }}</div>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</div>
