---
layout: archive
title: "News"
permalink: /news/
author_profile: true
redirect_from:
  - /updates
---

{% assign everything = site.publications | concat: site.talks %}
{% assign sorted = everything | sort: "date"%}

<ul>{% for post in sorted %}
  <b>{{post.date | date: "%m.%d.%y"}}</b>: 
  {% if post.collection == "publications" %}
    Our work, "{{post.title}}", was published at {{post.venueinformal}} <br>
  {% endif %}
  {% if post.collection == "talks" %}
    I gave a talk at {{post.venue}} called "{{post.title}}" <br>
  {% endif %}
{% endfor %}</ul>