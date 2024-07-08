---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>444.</div>
{% endif %}

{% include base_path %}

# 2023

{% for post in site.publications/2023 reversed %}
  {% include archive-single.html %}
{% endfor %}


# 2022

{% for post in site.publications/2022 reversed %}
  {% include archive-single.html %}
{% endfor %}
