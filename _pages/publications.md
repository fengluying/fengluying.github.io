---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% assign post_year = year %}
  {% if post_year != year %}
    {% assign current_year = post_year %}
      {% # year %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
