---
layout: archive
title: "Publications (First author)"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

## In submission

{% for post in site.publications reversed %}
  {% if post.in_submission == true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2025

{% for post in site.publications reversed %}
  {% if post.year == 2025 and post.in_submission != true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2024

{% for post in site.publications reversed %}
  {% if post.year == 2024 and post.in_submission != true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2023

{% for post in site.publications reversed %}
  {% if post.year == 2023 and post.in_submission != true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2022

{% for post in site.publications reversed %}
  {% if post.year == 2022 and post.in_submission != true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

