---
layout: default
---

<div class="section header-section">
  <h1>{{ site.title }}</h1>
  <p>{{ site.description }}</p>
</div>

<div class="section main-content">
  <div class="gallery-section">
    <div class="image-grid">
      {% for i in (1..4) %}
        <div class="image-item">
          <img src="{{ site.baseurl }}/images/mazda-3-2010 - {{ i }}.jpeg" alt="Mazda 3 Photo {{ i }}" loading="lazy" />
        </div>
      {% endfor %}
    </div>
    <a href="{{ site.baseurl }}/gallery" class="view-more">View More Images</a>
  </div>

  <div class="features-section">
    <h2>Car Features</h2>
    <ul>
      <li>Well-maintained with new components</li>
      <li>Paint in excellent condition</li>
      <li>No mechanical problems</li>
      <li>Recently serviced</li>
    </ul>
  </div>
</div>

<div class="section footer-section">
  <p>Contact me for more details or to schedule a viewing!</p>
</div>