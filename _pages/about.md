---
permalink: /
title: "About"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


Hello! I'm a fourth year PhD student in Computer Science at Northeastern University, and I am working with Malihe Alikhani. I am passionate about using NLP tools for good, and am currently studying bias in language through a sociolinguistic lens. I am also conducting research in the ethics space, and have an upcoming book chapter on ethics in signed languages. I have published at venues including ACL, NAACL, EACL, SIGDIAL, COLING, and COGSCI, and won a best paper award for our work at UAI 2022. Last year, I was part of a university team that placed third in the Amazon Alexa Prize Taskbot Competition!

News
======

{% assign everything = site.publications | concat: site.talks%}
{% assign sorted = everything | sort: "date" | reverse %}

<ul>{% for post in sorted | slice: 0, 5 %}
  <b>{{post.date | date: "%m.%d.%y"}}</b>: 
  {% if post.collection == "publications" %}
    Our work, "{{post.title}}", was published at {{post.venueinformal}} <br><br>
  {% endif %}
  {% if post.collection == "talks" %}
    I gave a talk at {{post.venue}} called "{{post.title}}" <br><br>
  {% endif %}
{% endfor %}</ul>