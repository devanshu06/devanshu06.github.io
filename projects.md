---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
classes: wide
search: true
---

A selection of systems, platforms, and tooling I’ve worked on or built.

<div class="grid__wrapper">
  {% for project in site.projects %}
    <div class="grid__item">
      <article class="archive__item">
        <h2 class="archive__item-title">
          <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
        </h2>
        <div class="archive__item-teaser">
          <img src="{{ project.header.teaser | relative_url }}" alt="">
        </div>
        <div class="archive__item-excerpt">
          {{ project.excerpt | markdownify }}
        </div>
      </article>
    </div>
  {% endfor %}
</div>
