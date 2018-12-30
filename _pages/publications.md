---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can view our publications since 2004 <u><a href="{{author.googlescholar}}">here</a>.</u>
{% endif %}

{% include base_path %}

{% if author.googlescholar %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
