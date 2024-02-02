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
      Our work, [{{post.title}}]({{post.paperurl}}), was published at {{post.venue}}\
    {% endif }
    {% if post.collection == "talks" %}:
      I gave a talk at **{{post.venue}}** called "{{post.title}}"\
  {% endfor %}</ul>