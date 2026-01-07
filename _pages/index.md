---
layout: default
permalink: /
title: ""
---

<div class="dash">
  <div class="dash__container">
    <div class="dash-grid">

      <!-- LEFT: Profile Card -->
      <aside class="dash-left">
        <div class="dash-card profile-card">

          <!-- Avatar (optional) -->
          <img
            class="avatar"
            src="{{ site.author.avatar | default: '/assets/images/avatar.jpg' | relative_url }}"
            alt="{{ site.author.name }}"
            onerror="this.style.display='none';"
          />

          <h1 class="profile-name">{{ site.author.name }}</h1>
          <p class="profile-sub">
            {{ site.description }}
          </p>

          <div class="cta-row">
            <a class="btnx btnx--light" href="{{ '/resume/' | relative_url }}">Resume</a>
            <a class="btnx btnx--dark" href="{{ '/contact/' | relative_url }}">Contact Me</a>
          </div>

          <div class="icon-row">
            {% if site.author.links %}
              {% for link in site.author.links %}
                <a class="icon-btn" href="{{ link.url }}" target="_blank" rel="noopener">
                  <i class="{{ link.icon }}"></i>
                </a>
              {% endfor %}
            {% endif %}
          </div>

        </div>
      </aside>

      <!-- RIGHT: Content Cards -->
      <section class="dash-right">

        <div class="dash-card">
          <h2>About Me</h2>
          <p>
            I’m a Data Analytics Engineering graduate student at George Mason University focused on predictive modeling,
            forecasting, and building dashboards that drive decision-making.
          </p>
        </div>

        <div class="dash-card">
          <h2>Skills</h2>
          <p style="opacity:.75; margin-top:-6px;">Tools, resources, and technologies I use often</p>
          <div class="projects-filters" style="margin-top:12px;">
            <span class="pill active">Python</span>
            <span class="pill">R</span>
            <span class="pill">SQL</span>
            <span class="pill">Machine Learning</span>
            <span class="pill">Tableau</span>
            <span class="pill">Power BI</span>
            <span class="pill">AWS</span>
          </div>
        </div>

        <div class="dash-card">
          <h2>Highlights</h2>
          <ul>
            <li><strong>120K+</strong> records analyzed; improved data quality by <strong>30%</strong>; reduced reporting time by <strong>40%</strong></li>
            <li>Forecasting &amp; optimization work that improved outcomes by <strong>10–15%</strong></li>
            <li>ML projects with strong predictive performance (R² up to <strong>0.85</strong>)</li>
          </ul>
        </div>

        <div class="dash-card">
          <h2>Featured Projects</h2>
          <p style="opacity:.8;">Start here, then see the full list on the Projects page.</p>
          <ul>
            <li><a href="{{ '/projects/disasterlens/' | relative_url }}">DisasterLens — Global Disaster Analysis</a></li>
            <li><a href="{{ '/projects/garment-worker-productivity/' | relative_url }}">Garment Worker Productivity Analysis</a></li>
            <li><a href="{{ '/projects/restaurant-revenue-prediction/' | relative_url }}">Restaurant Revenue Prediction</a></li>
          </ul>
        </div>

      </section>
    </div>
  </div>
</div>
