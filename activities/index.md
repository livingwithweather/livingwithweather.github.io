---
title: Activities
nav:
  order: 2
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Activities

This page displays information about recent eents. 

{% include tags.html tags="workshop, talk" %}

{% include search-info.html %}

{% include section.html %}

## Upcoming Activities

To be announced.

## Past Workshops

{% include list.html component="card" data="projects" filter="group == 'featured'" %}

{% include section.html %}

## Past Talks

{% include list.html component="card" data="projects" filter="!group" style="small" %}
