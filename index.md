---
layout: default
---

<header>
  <h1>{{ site.title }}</h1>
  <p>{{ site.description }}</p>
</header>

<div class="flex-container">
  <section class="gallery">
    <h2>Car Photos</h2>
    {% for i in (1..4) %}
      <a href="{{ site.baseurl }}/images/mazda-3-2010 - {{ i }}.jpeg" target="_blank">
        <img src="{{ site.baseurl }}/images/mazda-3-2010 - {{ i }}.jpeg" alt="Mazda 3 Photo {{ i }}" />
      </a>
    {% endfor %}
  </section>

  <section class="car-features">
    <h2>Car Features</h2>
    <ul>
      <li>Well-maintained with new components</li>
      <li>Paint in excellent condition</li>
      <li>No mechanical problems</li>
      <li>Recently serviced</li>
    </ul>
  </section>
</div>

<footer>
  <p>Contact me for more details or scan the QR code to visit this page again!</p>
</footer>