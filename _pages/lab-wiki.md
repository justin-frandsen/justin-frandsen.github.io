---
title: "Lab Wiki"
permalink: /lab-wiki/
layout: single
author_profile: false
sidebar:
  nav: "wiki"
excerpt: "Documentation, protocols, and how-to guides for the lab."
toc: false
---

Welcome to the lab wiki. EDIT THIS TEXT

<div class="grid__wrapper">

  {% assign wiki_topics = site.wiki | sort: "title" %}
  {% for topic in wiki_topics %}
  <div class="grid__item">
    <div class="card" style="padding: 20px; border-radius: 12px; background: #1e1e1e; min-height: 180px;">
      <h3 style="margin-top: 0;">
        <a href="{{ topic.url }}">{{ topic.title }}</a>
      </h3>
      <p>{{ topic.excerpt | strip_html | truncate: 160 }}</p>
    </div>
  </div>
  {% endfor %}

</div>

---

*Want to add or edit a page? Create a new Markdown file in the `_wiki/` folder and it will appear here automatically.*
