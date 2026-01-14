---
layout: dashboard
permalink: /
title: ""
---

<div class="dash__section dash__card">
  <h2 class="dash__h2">About Me</h2>
  <p class="dash__p">
    I’m a Data Analytics Engineering graduate student at George Mason University focused on predictive modeling,
    forecasting, and building dashboards that drive decision-making.
  </p>
</div>

<div class="dash__section dash__card">
  <h2 class="dash__h2">Skills</h2>
  <p class="dash__muted">Tools, resources, and technologies I use often</p>

  <div class="dash__chips">
    <span class="dash__chip">Python</span>
    <span class="dash__chip">R</span>
    <span class="dash__chip">SQL</span>
    <span class="dash__chip">Machine Learning</span>
    <span class="dash__chip">Tableau</span>
    <span class="dash__chip">Power BI</span>
    <span class="dash__chip">AWS</span>
  </div>
</div>

<div class="dash__section dash__card">
  <h2 class="dash__h2">Highlights</h2>

  <ul class="dash__list">
    <li><strong>120K+</strong> records analyzed; improved data quality by <strong>30%</strong>; reduced reporting time by <strong>40%</strong></li>
    <li>Forecasting &amp; optimization work that improved outcomes by <strong>10–15%</strong></li>
    <li>ML projects with strong predictive performance (R² up to <strong>0.85</strong>)</li>
  </ul>
</div>

<div class="dash__section dash__card">
  <div class="dash__row">
    <h2 class="dash__h2">Featured Projects</h2>
    <a class="dash__more" href="{{ '/projects/' | relative_url }}">View More</a>
  </div>

  <div class="projgrid">
    {% assign featured = site.projects | where: "featured", true %}
    {% for p in featured limit: 6 %}
      <a class="projcard" href="{{ p.url | relative_url }}">
        <div class="projcard__top">
          <div class="projcard__title">{{ p.title }}</div>
          <div class="projcard__link">View Project ↗</div>
        </div>

        {% if p.excerpt %}
          <div class="projcard__desc">{{ p.excerpt }}</div>
        {% endif %}

        {% if p.tech %}
          <div class="projcard__tags">
            {% for t in p.tech %}
              <span class="projtag">{{ t }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </a>
    {% endfor %}
  </div>
</div>

