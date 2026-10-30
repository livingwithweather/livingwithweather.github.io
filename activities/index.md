---
title: Activities
nav:
  order: 2
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Activities

This page displays information about recent events.

{% include tags.html tags="workshop, talk" %}

{% include search-info.html %}

{% include section.html %}

## Upcoming Activities

To be announced.

## Past Workshops

{% assign workshops = site.data.projects | where: "group", "featured" %}
<ul>
  {% for item in workshops %}
    <li>
      {% if item.link %}
        <a href="{{ item.link | relative_url | uri_escape }}">{{ item.title }}</a>
      {% else %}
        {{ item.title }}
      {% endif %}
      {% if item.date or item.subtitle %}
        <br>
        {% if item.date %}
          {{ item.date | date: "%d %B %Y" }}
        {% endif %}
        {% if item.subtitle %}
          {% if item.date %} — {% endif %}{{ item.subtitle }}
        {% endif %}
      {% endif %}
      {% if item.description %}
        <br>{{ item.description }}
      {% endif %}
    </li>
  {% endfor %}
</ul>

{% include section.html %}

## Past Talks

{% assign talks = site.data.projects | where_exp: "item", "item.group != 'featured'" %}
<ul>
  {% for item in talks %}
    <li>
      {% if item.link %}
        <a href="{{ item.link | relative_url | uri_escape }}">{{ item.title }}</a>
      {% else %}
        {{ item.title }}
      {% endif %}
      {% if item.date or item.subtitle %}
        <br>
        {% if item.date %}
          {{ item.date | date: "%d %B %Y" }}
        {% endif %}
        {% if item.subtitle %}
          {% if item.date %} — {% endif %}{{ item.subtitle }}
        {% endif %}
      {% endif %}
      {% if item.description %}
        <br>{{ item.description }}
      {% endif %}
    </li>
  {% endfor %}
</ul>

{% include section.html %}

## Gallery

<div style="display: flex; gap: 1rem; align-items: stretch; flex-wrap: wrap;">
  <div style="flex: 1 1 0; min-width: 220px;">
    {% include figure.html
      image="/assets/images/activity-1.jpg"
      caption="Activity 1"
      link="/"
      width="100%"
    %}
  </div>

  <div style="flex: 1 1 0; min-width: 220px;">
    {% include figure.html
      image="/assets/images/activity-2.jpg"
      caption="Activity 2"
      link="/"
      width="100%"
    %}
  </div>

  <div style="flex: 1 1 0; min-width: 220px;">
    {% include figure.html
      image="/assets/images/activity-3.jpg"
      caption="Activity 3"
      link="/"
      width="100%"
    %}
  </div>
</div>
