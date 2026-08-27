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

<style>
.wiki-scroll {
  display: flex;
  flex-direction: column;      /* stack items top to bottom */
  flex-wrap: nowrap;
  gap: 1em;
  padding-right: 1em;
}
.wiki-scroll__item {
  flex: 0 0 auto;
  width: 100%;
}
.wiki-scroll__item .card {
  height: 100%;
}
</style>

<div class="wiki-scroll">


  {% assign wiki_topics = site.wiki | sort: "title" %}
  {% for topic in wiki_topics %}
  <div class="wiki-scroll__item">
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


_*Want to add or edit a page? Create a new Markdown file in the_ `_wiki/` _folder and it will appear here automatically.*_