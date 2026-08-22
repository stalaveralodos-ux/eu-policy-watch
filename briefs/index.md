---
layout: default
title: EU Policy Watch
permalink: /briefs/
wide_layout: true
---
## What moved, month by month

A running archive: what actually happened across the files tracked on this site, one month at a time. Starts in August 2026.

<div class="digest-archive-grid">
{% assign sorted_digests = site.briefs | sort: 'month' | reverse %}
{% for d in sorted_digests %}
  <a class="digest-archive-card" href="{{ d.url | relative_url }}">
    <div class="digest-archive-month">{{ d.title }}</div>
    <p class="digest-archive-headline">{{ d.headline }}</p>
    <div class="digest-archive-count">{{ d.movers.size }} files moved</div>
  </a>
{% endfor %}
</div>
