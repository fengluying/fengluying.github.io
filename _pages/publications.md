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

# 2023

{% for post in site.publications reversed %}
  {% if post.year == 2023 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


# 2022

{% for post in site.publications.2022 reversed %}
  {% if post.year == 2022 %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
