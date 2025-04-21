---
layout: archive
title: "News"
permalink: /news/
author_profile: true
redirect_from:
  - /updates
---

{% assign everything = site.publications | concat: site.talks | concat: site.news %}
{% assign sorted = everything | sort: "date" | reverse %}

<div class="news">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">
<ul>{% for post in sorted %}
  <li><b>{{post.date | date: "%m.%d.%y"}}</b>: 
  {% if post.collection == "news" %}
    {{post.description}} 
  {% endif %}
  {% if post.collection == "publications" %}
    Our work, "{{post.title}}", was published at {{post.venueinformal}} <br><br>
  {% endif %}
  {% if post.collection == "talks" %}
    I gave a talk at {{post.venue}} called "{{post.title}}" <br><br>
  {% endif %}
  </li>
{% endfor %}</ul>
</div>