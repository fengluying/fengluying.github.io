---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>555.</div>
{% endif %}

{% include base_path %}

# 2024

{% for post in site.publications reversed %}
  {% if post.year == 2024 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


# 2023

{% for post in site.publications reversed %}
  {% if post.year == 2023 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
