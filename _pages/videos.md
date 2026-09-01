---
layout: archive
title: "Videos"
permalink: /videos/
author_profile: true
---

{% include base_path %}

{% if site.data.videos and site.data.videos.size > 0 %}
<div class="video-grid">
{% for video in site.data.videos %}
  <div class="video-grid__item">
    <div class="video-embed">
      <iframe src="https://www.youtube-nocookie.com/embed/{{ video.id }}" title="{{ video.title }}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
    </div>
    <p class="video-grid__caption">{{ video.title }}</p>
  </div>
{% endfor %}
</div>
{% else %}
<p>More videos coming soon — in the meantime, subscribe on <a href="https://www.youtube.com/{{ site.author.youtube }}">YouTube</a>.</p>
{% endif %}
