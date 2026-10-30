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
  <form action="https://formspree.io/f/xoeeloll" method="POST">
    <div style="margin-bottom: 1rem;">
      <label for="name" style="display: block; margin-bottom: 0.5rem; font-weight: 600;">Name</label>
      <input
        id="name"
        type="text"
        name="name"
        required
        style="width: 100%; padding: 0.75rem; border: 1px solid #ccc; border-radius: 6px; box-sizing: border-box;"
      >
    </div>

    <div style="margin-bottom: 1rem;">
      <label for="email" style="display: block; margin-bottom: 0.5rem; font-weight: 600;">Email</label>
      <input
        id="email"
        type="email"
        name="email"
        required
        style="width: 100%; padding: 0.75rem; border: 1px solid #ccc; border-radius: 6px; box-sizing: border-box;"
      >
    </div>

    <div style="margin-bottom: 1rem;">
      <label for="message" style="display: block; margin-bottom: 0.5rem; font-weight: 600;">Message</label>
      <textarea
        id="message"
        name="message"
        rows="6"
        required
        style="width: 100%; padding: 0.75rem; border: 1px solid #ccc; border-radius: 6px; box-sizing: border-box;"
      ></textarea>
    </div>

    <button
      type="submit"
      style="padding: 0.8rem 1.4rem; border: none; border-radius: 6px; background: #1f6feb; color: white; cursor: pointer;"
    >
      Send message
    </button>
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
