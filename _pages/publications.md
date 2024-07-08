---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>111.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% assign post_year = year %}
  {% if post_year != year %}
    {% assign current_year = post_year %}
      <div class="wordwrap"># {{year}}.</div>
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
