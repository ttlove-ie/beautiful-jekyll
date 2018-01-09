---
layout: page
title: gigs
subtitle: Born ready to rock <sup>TT</sup>love… Are you ready?
permalink: /gigs/
description: A growing collection of your cool gigs.
bigimg: /img/jonathan-jude-bike-logo-copy.jpg
---
<article>
  <div class="posts-list">
    {% for gig in site.gigs %}
    <article class="post-preview">
      <a href="{{ gig.url | prepend: site.baseurl }}">
  	  <h2 class="post-title">{{ gig.title }}</h2>

  	  {% if gig.subtitle %}
  	  <h3 class="song-subtitle">
  	    {{ gig.subtitle }}
  	  </h3>
  	  {% endif %}
      </a>

      <p class="song-meta">
        Posted on {{ gig.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry-container">
        {% if gig.image %}
        <div class="post-image">
          <a href="{{ gig.url | prepend: site.baseurl }}">
            <img src="{{ gig.image }}">
          </a>
        </div>
        {% endif %}
      </div>

      {% if gig.tags.size > 0 %}
      <div class="blog-tags">
        Tags:
        {% if gig.link-tags %}
        {% for tag in gig.tags %}
        <a href="{{ site.baseurl }}/tag/{{ tag }}">{{ tag }}</a>
        {% endfor %}
        {% else %}
          {{ gig.tags | join: ", " }}
        {% endif %}
      </div>
      {% endif %}
   </article>
  {% endfor %}
 </div>
