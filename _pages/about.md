---
permalink: /
title: "About"
layout: archive
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


Hello! I'm a fifth year PhD candidate in [Computer Science](https://www.khoury.northeastern.edu/) at [Northeastern University](https://www.northeastern.edu/), conducting research with [Malihe Alikhani](https://www.malihealikhani.com/). I am passionate about using NLP tools for good, and am currently studying bias in language through a sociolinguistic lens. I am also conducting research in the ethics space, and have an upcoming book chapter on ethics in signed languages. I have published at venues including ACL, NAACL, EACL, SIGDIAL, COLING, and COGSCI, and won a [best paper award](https://www.sci.pitt.edu/news/sci-graduate-students-faculty-member-win-best-paper-award-uai-2022) for our [work](https://proceedings.mlr.press/v180/sicilia22a/sicilia22a.pdf) at UAI 2022. Last year, I was part of a university team that placed [third](https://www.amazon.science/alexa-prize/taskbot-challenge/2022) in the Amazon [Alexa Prize Taskbot Competition](https://www.amazon.science/alexa-prize/taskbot-challenge)!

News
======

{% assign everything = site.publications | concat: site.talks%}
{% assign sorted = everything | sort: "date" | reverse %}

<div class="news">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">
<ul>{% for post in sorted limit:5 %}
  <li><b>{{post.date | date: "%m.%d.%y"}}</b>: 
  {% if post.collection == "publications" %}
    Our work, "{{post.title}}", was published at {{post.venueinformal}} 
  {% endif %}
  {% if post.collection == "talks" %}
    I gave a talk at {{post.venue}} called "{{post.title}}"
  {% endif %}</li>
{% endfor %}</ul>
</div>

[See more](katherine-atwell.github.io/news)
