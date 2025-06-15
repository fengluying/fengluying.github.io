---
permalink: /News/
title: "Latest News"
author_profile: true
redirect_from: 
  - /md/
  - /News.html
---

{% include base_path %}


<div class="volunteer-slider" style="max-width: 800px; margin: 0 auto; position: relative;">
  <h3 style="margin-top: 0;">Volunteer Moments</h3>
  <p>Volunteer memories preserved here.</p>
  
  <!-- 幻灯片容器 -->
  <div class="slides-container" style="position: relative; height: 400px; overflow: hidden;">
    <!-- 单个幻灯片 -->
    <div class="slide active" style="position: absolute; width: 100%; text-align: center; transition: opacity 0.5s;">
      <img src="/images/news/volunteer/CEC2025.jpg" width="500" alt="CEC Volunteer Event" style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>CEC Volunteer Program</strong><br>
        Hangzhou, June 12, 2025
      </div>
    </div>

    <div class="slide" style="position: absolute; width: 100%; text-align: center; transition: opacity 0.5s;">
      <img src="/images/news/volunteer/CCF2025.jpg" width="500" alt="CCF Volunteer Event" style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>CCF Community Service</strong><br>
        Hangzhou, January 17, 2025
      </div>
    </div>

    <div class="slide" style="position: absolute; width: 100%; text-align: center; transition: opacity 0.5s;">
      <img src="/images/news/volunteer/SES2024.jpg" width="500" alt="SES Volunteer Event" style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>SES Education Initiative</strong><br>
        Hangzhou, August 21, 2024
      </div>
    </div>

    <div class="slide" style="position: absolute; width: 100%; text-align: center; transition: opacity 0.5s;">
      <img src="/images/news/volunteer/DOCS2024.jpg" width="500" alt="DOCS Volunteer Event" style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
      <div class="slide-caption" style="margin-top: 1rem; font-style: italic; color: #555;">
        <strong>DOCS Healthcare Outreach</strong><br>
        Hangzhou, August 17, 2024
      </div>
    </div>
  </div>

  <!-- 导航按钮 -->
  <button class="slider-btn prev-btn" style="position: absolute; left: 10px; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px 15px; border-radius: 50%; cursor: pointer; z-index: 10;">❮</button>
  <button class="slider-btn next-btn" style="position: absolute; right: 10px; top: 50%; transform: translateY(-50%); background: rgba(0,0,0,0.5); color: white; border: none; padding: 10px 15px; border-radius: 50%; cursor: pointer; z-index: 10;">❯</button>

  <!-- 指示器 -->
  <div class="slider-indicators" style="text-align: center; margin-top: 15px;">
    <span class="indicator active" style="display: inline-block; width: 12px; height: 12px; border-radius: 50%; background: #333; margin: 0 5px; cursor: pointer;"></span>
    <span class="indicator" style="display: inline-block; width: 12px; height: 12px; border-radius: 50%; background: #ccc; margin: 0 5px; cursor: pointer;"></span>
    <span class="indicator" style="display: inline-block; width: 12px; height: 12px; border-radius: 50%; background: #ccc; margin: 0 5px; cursor: pointer;"></span>
    <span class="indicator" style="display: inline-block; width: 12px; height: 12px; border-radius: 50%; background: #ccc; margin: 0 5px; cursor: pointer;"></span>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const slides = document.querySelectorAll('.slide');
  const indicators = document.querySelectorAll('.indicator');
  const prevBtn = document.querySelector('.prev-btn');
  const nextBtn = document.querySelector('.next-btn');
  let currentIndex = 0;
  
  // 初始化幻灯片
  function showSlide(index) {
    slides.forEach((slide, i) => {
      slide.style.opacity = i === index ? '1' : '0';
      slide.style.zIndex = i === index ? '1' : '0';
    });
    
    indicators.forEach((indicator, i) => {
      indicator.style.background = i === index ? '#333' : '#ccc';
    });
  }
  
  // 下一张
  function nextSlide() {
    currentIndex = (currentIndex + 1) % slides.length;
    showSlide(currentIndex);
  }
  
  // 上一张
  function prevSlide() {
    currentIndex = (currentIndex - 1 + slides.length) % slides.length;
    showSlide(currentIndex);
  }
  
  // 按钮事件
  nextBtn.addEventListener('click', nextSlide);
  prevBtn.addEventListener('click', prevSlide);
  
  // 指示器点击事件
  indicators.forEach((indicator, index) => {
    indicator.addEventListener('click', () => {
      currentIndex = index;
      showSlide(currentIndex);
    });
  });
  
  // 自动播放
  let slideInterval = setInterval(nextSlide, 5000);
  
  // 鼠标悬停暂停
  const slider = document.querySelector('.volunteer-slider');
  slider.addEventListener('mouseenter', () => clearInterval(slideInterval));
  slider.addEventListener('mouseleave', () => {
    clearInterval(slideInterval);
    slideInterval = setInterval(nextSlide, 5000);
  });
  
  // 初始化显示第一张
  showSlide(0);
});
</script>