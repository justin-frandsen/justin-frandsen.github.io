---
title: "Research Projects"
permalink: /projects/
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: "0.2"
excerpt: "Current research projects in visual attention, statistical learning, and naturalistic perception."
---

<div class="grid__wrapper">

  {% for project in site.projects %}
  <div class="grid__item">
    <div class="card" style="padding: 20px; border-radius: 12px; background: #1e1e1e; min-height: 220px;">
      <h3 style="margin-top: 0;">
        <a href="{{ project.url }}">{{ project.title }}</a>
      </h3>
      <p>{{ project.excerpt | strip_html | truncate: 160 }}</p>
    </div>
  </div>
  {% endfor %}

</div>
