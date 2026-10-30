---
title: Activities
nav:
  order: 2
  tooltip: Workshops, public talks, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Activities

Community workshops, interviews, and research activities, along with public talks and speaking events. We are currently preparing a [Feedback](https://livingwithweather.github.io/activities/feedback) page, where participants will provide their thoughts and experiences with the Living With Weather (First Nations AI) project to-date. 

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
        <a href="{{ item.link | relative_url | uri_escape }}"><strong>{{ item.title }}</strong></a>
      {% else %}
        <strong>{{ item.title }}</strong>
      {% endif %}
      {% if item.date or item.subtitle %}
        <br>
        {% if item.date %}
          {{ item.date | date: "%d %B %Y" }}
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

{% include section.html %}

## Past Talks

{% assign talks = site.data.projects | where_exp: "item", "item.group != 'featured'" %}
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
          {{ item.date | date: "%d %B %Y" }}
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
