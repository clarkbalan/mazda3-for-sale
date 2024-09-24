---
layout: default
title: Image Gallery
---

<div class="section header-section">
  <img src="{{ site.baseurl }}/images/mazda-logo.png" alt="Mazda Logo" class="mazda-logo">
  <h1>{{ page.title }}</h1>
  <p>View all images of the 2010 Mazda 3</p>
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

function openLightbox(img) {
  document.getElementById("lightbox").style.display = "block";
  slideIndex = Array.from(img.parentNode.parentNode.children).indexOf(img.parentNode) + 1;
  showSlides(slideIndex);
}

function closeLightbox() {
  document.getElementById("lightbox").style.display = "none";
}

function changeSlide(n) {
  showSlides(slideIndex += n);
}

function showSlides(n) {
  let slides = document.getElementsByClassName("lightbox-slide");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (let i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  slides[slideIndex-1].style.display = "block";
}
</script>