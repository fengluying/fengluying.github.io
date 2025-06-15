---
permalink: /News/
title: "Latest News"
author_profile: true
redirect_from: 
  - /md/
  - /News.html
---

{% include base_path %}


<div class="news-content" style="padding: 1.2rem; max-width: 800px; margin: 0 auto;">
  <h3 style="margin-top: 0;">Volunteer Moments</h3>
  <p>Volunteer memories preserved here.</p>
  
  <div class="slider-container" style="position: relative; margin: 2rem 0;">
    <!-- Slides -->
    <div class="slide" style="display: none; text-align: center;">
      <img src="/images/news/volunteer/CEC2025.jpg" width="500" alt="CEC Volunteer Event" style="margin: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>CEC Volunteer Program</strong><br>
        Hangzhou, June 12, 2025
      </div>
    </div>

    <div class="slide" style="display: none; text-align: center;">
      <img src="/images/news/volunteer/CCF2025.jpg" width="500" alt="CCF Volunteer Event" style="margin: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>CCF Community Service</strong><br>
        Hangzhou, January 17, 2025
      </div>
    </div>

    <div class="slide" style="display: none; text-align: center;">
      <img src="/images/news/volunteer/SES2024.jpg" width="500" alt="SES Volunteer Event" style="margin: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>SES Education Initiative</strong><br>
        Hangzhou, August 21, 2024
      </div>
    </div>

    <div class="slide" style="display: none; text-align: center;">
      <img src="/images/news/volunteer/DOCS2024.jpg" width="500" alt="DOCS Volunteer Event" style="margin: auto; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>DOCS Healthcare Outreach</strong><br>
        Hangzhou, August 17, 2024
      </div>
    </div>

    <!-- Navigation buttons -->
    <button class="prev-btn" style="position: absolute; left: 10px; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px 15px; border-radius: 50%; cursor: pointer;">❮</button>
    <button class="next-btn" style="position: absolute; right: 10px; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px 15px; border-radius: 50%; cursor: pointer;">❯</button>
  </div>
</div>

<script>
  // Simple slider functionality
  document.addEventListener('DOMContentLoaded', function() {
    const slides = document.querySelectorAll('.slide');
    const prevBtn = document.querySelector('.prev-btn');
    const nextBtn = document.querySelector('.next-btn');
    let currentSlide = 0;
    
    // Show first slide
    slides[currentSlide].style.display = 'block';
    
    // Next slide function
    function nextSlide() {
      slides[currentSlide].style.display = 'none';
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].style.display = 'block';
    }
    
    // Previous slide function
    function prevSlide() {
      slides[currentSlide].style.display = 'none';
      currentSlide = (currentSlide - 1 + slides.length) % slides.length;
      slides[currentSlide].style.display = 'block';
    }
    
    // Button event listeners
    nextBtn.addEventListener('click', nextSlide);
    prevBtn.addEventListener('click', prevSlide);
    
    // Optional: Auto-advance slides every 5 seconds
    setInterval(nextSlide, 5000);
  });
</script>

<style>
  .slide {
    animation: fadeIn 0.5s;
  }
  
  @keyframes fadeIn {
    from {opacity: 0.4}
    to {opacity: 1}
  }
</style>
