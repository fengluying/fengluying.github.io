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
  {% if post.year == 0000 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2024

{% for post in site.publications reversed %}
  {% if post.year == 2024 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2023

{% for post in site.publications reversed %}
  {% if post.year == 2023 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2022

{% for post in site.publications reversed %}
  {% if post.year == 2022 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## 2020

{% for post in site.publications reversed %}
  {% if post.year == 2020 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
