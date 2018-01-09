---
layout: page
pagination:
  enabled: true
title: Billy
date: 2015-10-22 15:59:00-0400
inline: true
bigimg: /img/hello_world.jpeg
subtitle: Will you take me down again
youtubeId: yeFN3pOcuzc
tags:
  - Tom Wilde

image: /img/hello_world.jpeg
---

{% include youtubePlayer.html id=page.youtubeId %}

{% for item in site.songs %}
  <h2>{{ item.title }}</h2>
  <p>{{ item.subtitle }}</p>
  <p><a href="{{ item.url }}">{{ item.title }}</a></p>
{% endfor %}
