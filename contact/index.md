---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

<div style="max-width: 700px; margin: 2rem auto 0;">
  <form action="https://formspree.io/f/xoeeloll" method="POST" style="display: grid; gap: 1rem;">
    <div>
      <label for="name" style="display: block; margin-bottom: 0.5rem; font-family: var(--heading); font-weight: var(--semi-bold);">Name</label>
      <input
        id="name"
        type="text"
        name="name"
        required
        style="width: 100%; height: 40px; margin: 0; padding: 5px 10px; border: solid 1px var(--light-gray); border-radius: var(--rounded); background: var(--background); color: var(--text); font-family: inherit; font-size: inherit; appearance: none; box-shadow: var(--shadow); box-sizing: border-box;"
      >
    </div>

    <div>
      <label for="email" style="display: block; margin-bottom: 0.5rem; font-family: var(--heading); font-weight: var(--semi-bold);">Email</label>
      <input
        id="email"
        type="email"
        name="email"
        required
        style="width: 100%; height: 40px; margin: 0; padding: 5px 10px; border: solid 1px var(--light-gray); border-radius: var(--rounded); background: var(--background); color: var(--text); font-family: inherit; font-size: inherit; appearance: none; box-shadow: var(--shadow); box-sizing: border-box;"
      >
    </div>

    <div>
      <label for="message" style="display: block; margin-bottom: 0.5rem; font-family: var(--heading); font-weight: var(--semi-bold);">Message</label>
      <textarea
        id="message"
        name="message"
        rows="6"
        required
        style="width: 100%; min-height: 140px; margin: 0; padding: 8px 10px; border: solid 1px var(--light-gray); border-radius: var(--rounded); background: var(--background); color: var(--text); font-family: inherit; font-size: inherit; appearance: none; box-shadow: var(--shadow); box-sizing: border-box; resize: vertical;"
      ></textarea>
    </div>

    <div style="display: flex; justify-content: flex-start;">
      <button class="button" type="submit">Send message</button>
    </div>
  </form>
</div>

{%
  include button.html
  type="address"
  tooltip="Our location on Google Maps for easy navigation"
  link="https://www.google.com/maps"
%}

{% include section.html %}

{% capture col1 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption="Lorem ipsum"
%}

{% endcapture %}

{% capture col2 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption="Lorem ipsum"
%}

{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}

{% include section.html dark=true %}

{% capture col1 %}
Lorem ipsum dolor sit amet  
consectetur adipiscing elit  
sed do eiusmod tempor
{% endcapture %}

{% capture col2 %}
Lorem ipsum dolor sit amet  
consectetur adipiscing elit  
sed do eiusmod tempor
{% endcapture %}

{% capture col3 %}
Lorem ipsum dolor sit amet  
consectetur adipiscing elit  
sed do eiusmod tempor
{% endcapture %}

{% include cols.html col1=col1 col2=col2 col3=col3 %}
