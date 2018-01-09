---
layout: page
title: Songs
subtitle: It's hard to win without sinning and it's hard to find somebody to <sup>TT</sup>love…
permalink: /projects/
description: A growing collection of your cool projects.
bigimg: /img/jonathan-jude-bike-logo-copy.jpg
---

{% for song in site.songs %}
<div>
    <div>

        <span>
            <h1>{{ song.title }}</h1>
            <br/>
            <p>{{ song.subtitle }}</p>
        </span>
        </a>
    </div>
</div>

{% endfor %}
