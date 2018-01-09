---
layout: page
title: Songs
subtitle: It's hard to win without sinning and it's hard to find somebody to <sup>TT</sup>love…
permalink: /songs/
description: A growing collection of your cool songs.
bigimg: /img/jonathan-jude-bike-logo-copy.jpg
---
<article>
  <div class="songs-list">
    {% for song in site.songs %}
    <article class="post-preview">
      <a href="{{ song.url | prepend: site.baseurl }}">
  	  <h2 class="post-title">{{ song.title }}</h2>

  	  {% if song.subtitle %}
  	  <h3 class="song-subtitle">
  	    {{ song.subtitle }}
  	  </h3>
  	  {% endif %}
      </a>

      <p class="song-meta">
        Posted on {{ song.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry-container">
        {% if song.image %}
        <div class="post-image">
          <a href="{{ song.url | prepend: site.baseurl }}">
            <img src="{{ song.image }}">
          </a>
        </div>
        {% endif %}
      </div>

      {% if song.tags.size > 0 %}
      <div class="blog-tags">
        Tags:
        {% if song.link-tags %}
        {% for tag in song.tags %}
        <a href="{{ site.baseurl }}/tag/{{ tag }}">{{ tag }}</a>
        {% endfor %}
        {% else %}
          {{ song.tags | join: ", " }}
        {% endif %}
      </div>
      {% endif %}
   </article>
  {% endfor %}
 </div>
