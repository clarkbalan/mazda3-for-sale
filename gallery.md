---
layout: default
title: Image Gallery
---

<div class="section header-section">
  <img src="{{ site.baseurl }}/images/mazda-logo.png" alt="Mazda Logo" class="mazda-logo">
  <h1>{{ page.title }}</h1>
  <a href="{{ site.baseurl }}/" class="view-more">Back to Main Page</a>
</div>

<div class="section main-content gallery-page">
  <div class="gallery-section">
    <div class="image-grid">
      {% for image in site.static_files %}
        {% if image.path contains 'images/mazda-3-2010' %}
          <div class="image-item">
            <img src="{{ site.baseurl }}{{ image.path }}" alt="Mazda 3 Photo" loading="lazy" onclick="openLightbox(this)" />
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<div id="lightbox" class="lightbox">
  <span class="close cursor" onclick="closeLightbox()">&times;</span>
  <div class="lightbox-content">
    {% for image in site.static_files %}
      {% if image.path contains 'images/mazda-3-2010' %}
        <div class="lightbox-slide">
          <img src="{{ site.baseurl }}{{ image.path }}" alt="Mazda 3 Photo">
        </div>
      {% endif %}
    {% endfor %}
  </div>
  <a class="prev" onclick="changeSlide(-1)">&#10094;</a>
  <a class="next" onclick="changeSlide(1)">&#10095;</a>
</div>

<div class="section footer-section">
  <p>Contact me for more details or to schedule a viewing!</p>
</div>

<script>
let slideIndex = 1;
let slides = document.getElementsByClassName("lightbox-slide");

function openLightbox(img) {
  document.getElementById("lightbox").style.display = "block";
  const imgSrc = img.src;
  
  // Set the clicked image as the only visible slide
  for (let i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
    if (slides[i].getElementsByTagName('img')[0].src === imgSrc) {
      slides[i].style.display = "block";
      slideIndex = i + 1; // Set the index based on the clicked image
    }
  }
}

function closeLightbox() {
  document.getElementById("lightbox").style.display = "none";
}

function changeSlide(n) {
  showSlides(slideIndex += n);
}

function showSlides(n) {
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  
  // Hide all slides
  for (let i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  // Show the current slide
  slides[slideIndex-1].style.display = "block";
}
</script>

<div class="price-drop">
  <p class="original-price">Original Price: <span>$6,200</span></p>
  <p class="new-price">New Price: <span>$5,600</span></p>
  <p class="savings">Save 10% - That's $600 off!</p>
</div>

<!-- Contact Info Box -->
<div class="contact-info-box">
  <p>For inquiries, you can reach me:</p>
  <ul>
    <li><strong>Phone Calls:</strong> 5 PM - 10 PM at <a href="tel:+13852460055">385-246-0055</a></li>
    <li><strong>Text:</strong> Anytime at <a href="sms:+13852460055">385-246-0055</a></li>
    <li><strong>Email:</strong> <a href="mailto:mazda3forsale@sudomail.com">mazda3forsale@sudomail.com</a></li>
  </ul>
</div>

<style>
.price-drop {
    background-color: #e74c3c;
    color: white;
    padding: 20px;
    border-radius: 10px;
    margin-top: 20px;
    display: inline-block;
    text-align: center;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.contact-info-box {
    background-color: #4CAF50; /* Green background */
    color: white;
    padding: 20px;
    border-radius: 10px;
    margin-top: 20px;
    text-align: center;
    font-size: 1.1rem;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.contact-info-box ul {
    list-style-type: none;
    padding-left: 0;
}

.contact-info-box li {
    margin-bottom: 10px;
}
</style>
