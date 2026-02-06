---
layout: default
title: Projects
permalink: /projects/
---

<div class="container" style="padding: 60px 0;">
  <h1 style="margin-bottom: 18px;">Projects</h1>
  <p style="opacity:0.8; margin-bottom: 30px;">
    Selected robotics projects including proximity sensing, reactive control, and HRI safety.
  </p>

  <div class="features-list">
    {% assign sorted = site.projects | sort: "date" | reverse %}
    {% for p in sorted %}
      <div class="feature-item">
        <h3 style="margin-bottom: 8px;">
          <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
        </h3>
        <p style="margin:0; opacity:0.85;">
          {{ p.excerpt | strip_html | truncate: 160 }}
        </p>
        <p style="margin-top:10px; opacity:0.7; font-size: 0.95em;">
          {{ p.date | date: "%b %Y" }} · {{ p.categories | join: ", " }}
        </p>
      </div>
    {% endfor %}
  </div>
</div>
