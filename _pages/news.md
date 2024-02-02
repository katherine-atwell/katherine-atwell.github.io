---
layout: archive
title: "News"
permalink: /news/
author_profile: true
redirect_from:
  - /updates
---

{% assign everything = site.publications | concat: site.talks %}

<ul>{% for post in everything %}
    {{post.date}}
  {% endfor %}</ul>