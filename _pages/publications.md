---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


{% if page.author and site.data.authors[page.author] %}
  {% assign author = site.data.authors[page.author] %}{% else %}{% assign author = site.author %}
{% endif %}

{% if author.googlescholar %}
  You can view our publications since 2004 <u><a href="{{author.googlescholar}}">here</a>.</u>
{% endif %}

{% include base_path %}

{% if author.googlescholar %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
