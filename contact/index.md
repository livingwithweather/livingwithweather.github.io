---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

Thank you for your interest in our research. Our team are primarily based at [Charles Darwin University](https://www.cdu.edu.au/northern-institute/study/phd-master-research), in Garramilla (Darwin, Northern Territory, Australia).

Key members of our team also contribute remotely from across Australia - in Naarm (Melbourne, VIC) and Kaurna (Adelaide, SA) - as well as internationally, in Manila (the Philippines). 

Please feel free to use our contact form below to get in touch. We look forward to hearing from you. 

<div style="max-width: 700px; margin: 2rem auto 0;">
  <form id="contact-form" action="https://formspree.io/f/xoeeloll" method="POST" style="display: grid; gap: 1rem;">
    <div id="form-status" aria-live="polite" style="display: none; padding: 0.75rem 1rem; border-radius: var(--rounded); background: rgba(0,0,0,0.04); color: var(--text); font-family: var(--heading); font-weight: var(--semi-bold);"></div>

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

<div style="max-width: 700px; margin: 1.5rem auto 0;">
  <img
    src="/images/contact2.jpg"
    alt="Contact page image"
    style="width: 100%; height: auto; display: block; border-radius: var(--rounded);"
  >
</div>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    var form = document.getElementById('contact-form');
    var status = document.getElementById('form-status');

    if (!form || !status) return;

    form.addEventListener('submit', function (event) {
      event.preventDefault();

      status.textContent = 'Sending your message...';
      status.style.display = 'block';
      status.style.background = 'rgba(0,0,0,0.04)';
      status.style.color = 'var(--text)';

      fetch(form.action, {
        method: 'POST',
        body: new FormData(form),
        headers: {
          'Accept': 'application/json'
        }
      })
      .then(function (response) {
        if (response.ok) {
          form.reset();
          form.style.display = 'none';
          status.textContent = 'Thanks! Your message has been sent.';
          status.style.background = 'rgba(12, 130, 76, 0.08)';
          status.style.color = 'var(--primary)';
          return;
        }

        throw new Error('Submission failed');
      })
      .catch(function () {
        status.textContent = 'Something went wrong. Please try again or email livingwithweather@outlook.com.';
        status.style.background = 'rgba(180, 0, 0, 0.05)';
        status.style.color = 'var(--text)';
      });
    });
  });
</script>
