---
permalink: /News/
title: "Latest News"
author_profile: true
redirect_from: 
  - /md/
  - /News.html
---

{% include base_path %}

<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Volunteer Moments</title>
  <style>
    .volunteer-slider {
      max-width: 800px;
      margin: 0 auto;
      position: relative;
      font-family: sans-serif;
    }

    .slides-container {
      position: relative;
      height: 700px;
      overflow: hidden;
    }

    .slide {
      position: absolute;
      width: 100%;
      height: 100%;
      text-align: center;
      opacity: 0;
      z-index: 0;
      transition: opacity 0.5s ease;
      pointer-events: none;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

    .slide.active {
      opacity: 1;
      z-index: 1;
      pointer-events: auto;
    }

    .slide img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .slide-caption {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(255, 255, 255, 0.8);
      padding: 10px 20px;
      border-radius: 8px;
      font-style: italic;
      color: #333;
      z-index: 2;
      max-width: 90%;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
    }

    .slider-btn {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: rgba(0, 0, 0, 0.5);
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 50%;
      cursor: pointer;
      z-index: 10;
    }

    .prev-btn { left: 10px; }
    .next-btn { right: 10px; }

    .slider-indicators {
      text-align: center;
      margin-top: 15px;
    }

    .indicator {
      display: inline-block;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: #ccc;
      margin: 0 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .indicator.active {
      background: #333;
    }
  </style>
</head>
<body>

<div class="volunteer-slider">
  <h3 style="margin-top: 0;">Volunteer Moments</h3>
  <p>Volunteer memories preserved here.</p>

  <div class="slides-container">
    <div class="slide active">
      <img src="/images/news/volunteer/CEC2025.jpg">
      <div class="slide-caption">
        <strong>CEC 2025</strong><br>
        Hangzhou, June 12, 2025
      </div>
    </div>

    <div class="slide">
      <img src="/images/news/volunteer/CCF2025.jpg">
      <div class="slide-caption">
        <strong>CCF-AI演化学组成立大会</strong><br>
        Hangzhou, January 17, 2025
      </div>
    </div>

    <div class="slide">
      <img src="/images/news/volunteer/SES2024.jpg">
      <div class="slide-caption">
        <strong>SES 2024</strong><br>
        Hangzhou, August 21, 2024
      </div>
    </div>

    <div class="slide">
      <img src="/images/news/volunteer/DOCS2024.jpg">
      <div class="slide-caption">
        <strong>DOCS 2024</strong><br>
        Hangzhou, August 17, 2024
      </div>
    </div>
  </div>

  <button class="slider-btn prev-btn">❮</button>
  <button class="slider-btn next-btn">❯</button>

  <div class="slider-indicators">
    <span class="indicator active"></span>
    <span class="indicator"></span>
    <span class="indicator"></span>
    <span class="indicator"></span>
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    const slides = document.querySelectorAll('.slide');
    const indicators = document.querySelectorAll('.indicator');
    const prevBtn = document.querySelector('.prev-btn');
    const nextBtn = document.querySelector('.next-btn');
    let currentIndex = 0;
    let slideInterval;

    function showSlide(index) {
      slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
      });
      indicators.forEach((indicator, i) => {
        indicator.classList.toggle('active', i === index);
      });
    }

    function nextSlide() {
      currentIndex = (currentIndex + 1) % slides.length;
      showSlide(currentIndex);
    }

    function prevSlide() {
      currentIndex = (currentIndex - 1 + slides.length) % slides.length;
      showSlide(currentIndex);
    }

    nextBtn.addEventListener('click', nextSlide);
    prevBtn.addEventListener('click', prevSlide);

    indicators.forEach((indicator, index) => {
      indicator.addEventListener('click', () => {
        currentIndex = index;
        showSlide(currentIndex);
      });
    });

    function startAutoSlide() {
      slideInterval = setInterval(nextSlide, 5000);
    }

    function stopAutoSlide() {
      clearInterval(slideInterval);
    }

    const slider = document.querySelector('.volunteer-slider');
    slider.addEventListener('mouseenter', stopAutoSlide);
    slider.addEventListener('mouseleave', startAutoSlide);

    showSlide(currentIndex);
    startAutoSlide();
  });
</script>

</body>
</html>