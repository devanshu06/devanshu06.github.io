---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
classes: wide
search: true
collection: projects
---

A selection of systems, platforms, and tooling I’ve worked on or built.

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}
