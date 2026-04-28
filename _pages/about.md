---
permalink: /
title: "Luying Feng, PhD."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## Education background
Hi there! I am a PhD student in Computer Science and Engineering at Westlake University, advised by [Prof. Yaochu Jin](https://en.westlake.edu.cn/faculty/yaochu-jin.html). I received my master's degree in Mechanical Engineering from Zhejiang University in 2024, where I worked with [Prof. Canjun Yang](https://person.zju.edu.cn/ycj) and [Prof. Wei Yang](https://www.labxing.com/profile/121680). I earned my bachelor's degree in Mechanical and Electronic Engineering from Jiangnan University in 2021, advised by [Prof. Xueliang Ping](https://baike.baidu.com/item/%E5%B9%B3%E9%9B%AA%E8%89%AF/1915219).

## Research interests
My research interests lie at the intersection of robotics, human-machine interaction, and embodied intelligence. I am currently working on brain-inspired embodied intelligence and general-purpose loco-manipulation. Through my research, I aim to build methods that can better understand and model human brain and humanoid motion, and enable robust interaction between intelligent agents and the physical world. 

## My companions

<style>
.pet-section {
  display: flex;
  gap: 18px;
  align-items: flex-start;
  margin: 18px 0 26px;
}
.pet-carousel {
  width: 320px;
  max-width: 45%;
  aspect-ratio: 4 / 3;
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  background: #f5f5f5;
}
.pet-carousel .slide {
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity 0.6s ease;
}
.pet-carousel .slide.active {
  opacity: 1;
}
.pet-carousel img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}
.pet-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 34px;
  height: 34px;
  border: none;
  border-radius: 50%;
  background: rgba(0, 0, 0, 0.45);
  color: #fff;
  font-size: 20px;
  line-height: 34px;
  text-align: center;
  cursor: pointer;
  z-index: 2;
}
.pet-nav.prev { left: 8px; }
.pet-nav.next { right: 8px; }
.pet-text {
  flex: 1;
  min-width: 220px;
}
@media (max-width: 800px) {
  .pet-section {
    flex-direction: column;
  }
  .pet-carousel {
    width: 100%;
    max-width: 100%;
  }
}
</style>

{% assign peds_images = site.static_files | where_exp: "f", "f.path contains '/images/peds/'" | sort: "path" %}
{% assign friends_images = site.static_files | where_exp: "f", "f.path contains '/images/friends/'" | sort: "path" %}

<div class="pet-section">
  <div class="pet-carousel" data-carousel data-interval="4200">
    {% for img in peds_images %}
      <div class="slide{% if forloop.first %} active{% endif %}">
        <img src="{{ img.path | relative_url }}" alt="JoJo photo {{ forloop.index }}">
      </div>
    {% endfor %}
    <button class="pet-nav prev" type="button" aria-label="Previous">‹</button>
    <button class="pet-nav next" type="button" aria-label="Next">›</button>
  </div>
  <div class="pet-text">
    <h3 style="margin-top: 0;">My favorite pet JoJo</h3>
    <p>JoJo is my favorite pet and brings me joy every day.</p>
  </div>
</div>

<div class="pet-section">
  <div class="pet-carousel" data-carousel data-interval="4500">
    {% for img in friends_images %}
      <div class="slide{% if forloop.first %} active{% endif %}">
        <img src="{{ img.path | relative_url }}" alt="Bazong photo {{ forloop.index }}">
      </div>
    {% endfor %}
    <button class="pet-nav prev" type="button" aria-label="Previous">‹</button>
    <button class="pet-nav next" type="button" aria-label="Next">›</button>
  </div>
  <div class="pet-text">
    <h3 style="margin-top: 0;">My closest partner Bazong</h3>
    <p>Bazong is my closest partner, accompanying me through all the ups and downs of research.</p>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var carousels = document.querySelectorAll("[data-carousel]");
  carousels.forEach(function (carousel) {
    var slides = carousel.querySelectorAll(".slide");
    if (slides.length <= 1) return;
    var idx = 0;
    var interval = parseInt(carousel.getAttribute("data-interval") || "3000", 10);
    function show(nextIdx) {
      slides[idx].classList.remove("active");
      idx = (nextIdx + slides.length) % slides.length;
      slides[idx].classList.add("active");
    }
    var timer = setInterval(function () {
      show(idx + 1);
    }, interval);
    var prevBtn = carousel.querySelector(".pet-nav.prev");
    var nextBtn = carousel.querySelector(".pet-nav.next");
    if (prevBtn) {
      prevBtn.addEventListener("click", function () {
        show(idx - 1);
      });
    }
    if (nextBtn) {
      nextBtn.addEventListener("click", function () {
        show(idx + 1);
      });
    }
  });
});
</script>

