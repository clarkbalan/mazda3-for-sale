---
layout: default
---

<div class="section header-section">
  <img src="{{ site.baseurl }}/images/mazda-logo.png" alt="Mazda Logo" class="mazda-logo">
  <h1 class="main-title">2010 Mazda 3 <span class="subtitle">A Premium Driving Experience</span></h1>
  
  <div class="car-highlights">
    <p><span class="highlight">Excellent Condition</span> | <span class="highlight">195K Miles</span> | <span class="highlight">2.5 S Model</span></p>
    <p class="no-issues">✓ No Mechanical Issues</p>
  </div>

  <div class="price-drop">
    <p class="original-price">Original Price: <span>$6,200</span></p>
    <p class="new-price">New Price: <span>$5,600</span></p>
    <p class="savings">Save 10% - That's $600 off!</p>
  </div>
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