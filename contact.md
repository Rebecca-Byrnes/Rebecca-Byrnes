---
layout: default
title: Contact Me
permalink: /contact/
---

## Contact Me

I’m open to consulting, full‑time roles, and collaborations.

- LinkedIn: <a href="https://www.linkedin.com/in/rebeccabyrnes" target="_blank" rel="noopener">linkedin.com/in/rebeccabyrnes</a>
- GitHub: <a href="https://github.com/Rebecca-Byrnes" target="_blank" rel="noopener">github.com/Rebecca-Byrnes</a>
- Location: Portugal (EU‑friendly time zones)

### Send a message

<form id="contact-form" class="contact-form" action="https://formspree.io/f/mkgvlwko" method="POST">
  <input type="hidden" name="_subject" value="New message from rebeccabyrnes.site" />
  <div class="form-group">
    <label for="name">Name</label>
    <input id="name" name="name" type="text" required />
  </div>
  <div class="form-group">
    <label for="email">Email</label>
    <input id="email" name="email" type="email" required />
  </div>
  <div class="form-group">
    <label for="message">Message</label>
    <textarea id="message" name="message" rows="6" required></textarea>
  </div>
  <div class="form-group">
    <div class="g-recaptcha" data-sitekey="6LcphcsrAAAAAOoq4y3ImX9A24LXm_41KbQTIY9S"></div>
  </div>
  <button class="button" type="submit">Send</button>
  <p id="form-status" class="form-status" aria-live="polite" hidden></p>
</form>

<script src="https://www.google.com/recaptcha/api.js" async defer></script>
<script>
  (function() {
    var form = document.getElementById('contact-form');
    var statusEl = document.getElementById('form-status');
    function showStatus(msg, ok) {
      statusEl.hidden = false;
      statusEl.textContent = msg;
      statusEl.className = 'form-status ' + (ok ? 'ok' : 'err');
    }
    form.addEventListener('submit', function(e) {
      var resp = window.grecaptcha && window.grecaptcha.getResponse ? window.grecaptcha.getResponse() : '';
      if (!resp) {
        e.preventDefault();
        showStatus('Please complete the CAPTCHA.', false);
      }
    });
  })();
</script>


