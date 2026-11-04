---
title: Activities
nav:
  order: 2
  tooltip: Workshops, public talks, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Activities

<p class="page-intro page-intro-left">Community workshops, interviews, and research activities, along with public talks and speaking events. We are currently preparing a <a href="https://livingwithweather.github.io/activities/feedback">Feedback</a> page, where participants will provide their thoughts and experiences with the Living With Weather (First Nations AI) project to-date.</p>

{% include search-info.html %}

{% include section.html %}

## Upcoming Activities

To be announced.

## Past Workshops

{% assign workshops = site.data.projects | where: "group", "featured" %}
{% assign workshop_years = "2025,2024,2023" | split: "," %}
{% for year in workshop_years %}
  {% assign year_prefix = year | append: " | " %}
  {% assign yearly_workshops = workshops | where_exp: "item", "item.title contains year_prefix" %}
  {% if yearly_workshops.size > 0 %}

<h3 style="font-size: 1.15em; margin: 1em 0 0.4em;">{{ year }}</h3>

<ul>
  {% for item in yearly_workshops %}
    <li>
      {% assign display_title = item.title | remove_first: year_prefix %}
      {% if item.link %}
        <a href="{{ item.link | relative_url | uri_escape }}"><strong>{{ display_title }}</strong></a>
      {% else %}
        <strong>{{ display_title }}</strong>
      {% endif %}
      {% if item.date or item.subtitle %}
        <br>
        {% if item.date %}
          {% assign date_range = item.date | split: " to " %}
          {% if date_range.size > 1 %}
            {{ date_range[0] | date: "%-d %B %Y" }} – {{ date_range[1] | date: "%-d %B %Y" }}
          {% else %}
            {{ item.date | date: "%d %B %Y" }}
          {% endif %}
        {% endif %}
        {% if item.subtitle %}
          {% if item.date %} — {% endif %}<em>{{ item.subtitle }}</em>
        {% endif %}
      {% endif %}
      {% if item.description %}
        <br>{{ item.description }}
      {% endif %}
    </li>
  {% endfor %}
</ul>
  {% endif %}
{% endfor %}

{% assign talks = site.data.projects | where_exp: "item", "item.group != 'featured'" %}
{% if talks.size > 0 %}
  {% include section.html %}

  ## Past Talks

  <ul>
    {% for item in talks %}
      <li>
        {% if item.link %}
          <a href="{{ item.link | relative_url | uri_escape }}"><strong>{{ item.title }}</strong></a>
        {% else %}
          <strong>{{ item.title }}</strong>
        {% endif %}
        {% if item.date or item.subtitle %}
          <br>
          {% if item.date %}
            {% assign date_range = item.date | split: " to " %}
            {% if date_range.size > 1 %}
              {{ date_range[0] | date: "%-d %B %Y" }} – {{ date_range[1] | date: "%-d %B %Y" }}
            {% else %}
              {{ item.date | date: "%d %B %Y" }}
            {% endif %}
          {% endif %}
          {% if item.subtitle %}
            {% if item.date %} — {% endif %}<em>{{ item.subtitle }}</em>
          {% endif %}
        {% endif %}
        {% if item.description %}
          <br>{{ item.description }}
        {% endif %}
      </li>
    {% endfor %}
  </ul>
{% endif %}

{% include section.html %}

## Gallery

<div style="display: flex; gap: 1rem; align-items: stretch; flex-wrap: wrap;">
  <div style="flex: 1 1 0; min-width: 220px;">
    {% include figure.html
      image="/images/Warruwi1.jpg"
      caption="Photo: Jens Cheung, _Warruwi Workshop (July 2025)_"
      link="/"
      width="100%"
    %}
  </div>

  <div style="flex: 1 1 0; min-width: 220px;">
    {% include figure.html
      image="/images/Warruwi2.jpg"
      caption="Photo: Jens Cheung, _Warruwi Workshop (July 2025)_"
      link="/"
      width="100%"
    %}
  </div>

  <div style="flex: 1 1 0; min-width: 220px;">
    {% include figure.html
      image="/images/Warruwi3.jpg"
      caption="Photo: Jens Cheung, _Warruwi Workshop (July 2025)_"
      link="/"
      width="100%"
    %}
  </div>
</div>
