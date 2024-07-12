---
layout: page
title: Playlists
permalink: /playlists/
description: Good tunes for your ears
note: Click a list for more info, and sometimes a link to listen.
homepage_show: true
homepage:
  text: "Art in three dimensions: cardboard, paper mâché, wood, and found object"
  icon: fas fa-music
  image: assets/images/tape.png
pagination:
  enabled: true
  per_page: 100
  categories:
   values:
     - Xmas-Mix
     - Playlist
   matching: any
---

<ul id="playlist" class="blob-grid-4 image-only">
{% assign playlists = paginator.posts | sort:"date" | reverse %}
{% for post in playlists %}
    <li class="colorway">
        <a href="{{ post.url | relative_url }}" title="{{post.title}}">
            <img src="{{post.image}}" alt="{{post.title}}"/>
        </a>
    </li>
{% endfor %}
</ul>
