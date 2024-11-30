---
layout: archive
title: "News"
permalink: /news/
author_profile: true
redirect_from:
  - /updates
---

{% assign everything = site.publications | concat: site.talks%}
{% assign sorted = everything | sort: "date" | reverse %}

<ul>{% for post in sorted %}
  <li><i class="fa fa-w newspaper-o"> </i> <b>{{post.date | date: "%m.%d.%y"}}</b>: 
  {% if post.collection == "publications" %}
    Our work, "{{post.title}}", was published at {{post.venueinformal}} <br><br>
  {% endif %}
  {% if post.collection == "talks" %}
    I gave a talk at {{post.venue}} called "{{post.title}}" <br><br>
  {% endif %}
  </li>
{% endfor %}</ul>