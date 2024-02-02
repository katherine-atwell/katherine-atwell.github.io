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
    {{post.date | date: ‘%d/%m/%y’}}: 
    {% if post.collection == "publications" %}
      Our work, <b>{{post.title}}</b>, was published at {{post.venueinformal}}\

    {% endif %}
    {% if post.collection == "talks" %}:
      I gave a talk at <b>{{post.venue}}</b> called "{{post.title}}"\

    {% endif %}
  {% endfor %}</ul>