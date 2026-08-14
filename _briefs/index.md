---
layout: default
title: EU Policy Watch
permalink: /briefs/
---
## What is the Commission doing now?
A running log of the legislative files shaping Brussels in 2026, tracked as they move through Parliament and Council.
The <a href="https://commission.europa.eu/document/download/05d3777d-5d73-456d-bf56-38caa77d53c8_en?filename=2025-CWP_0.pdf" target="_blank">Commission's 2026 Work Programme</a> sets out 47 legislative initiatives, with simplification as the central thread: more than half carry a strong simplification component, building on the omnibus approach already used for sustainability reporting and now extended to digital rules, energy product legislation, taxation and citizens' rules. Alongside simplification, the programme leans into competitiveness (following the <a href="https://commission.europa.eu/document/download/97e481fd-2dc3-412d-be4c-f152a8232961_en?filename=The%20future%20of%20European%20competitiveness%20_%20A%20competitiveness%20strategy%20for%20Europe.pdf" target="_blank">Draghi report</a>), defence readiness by 2030, and a comprehensive push on migration and returns.
This page tracks the files worth watching, one brief at a time: where each stands, what is at stake for those affected, and what to watch next.
### Briefs
<ul class="brief-list">
{% assign sorted_briefs = site.briefs | sort: 'date' | reverse %}
{% for brief in sorted_briefs %}
  <li>
    <span class="topic-tag topic-{{ brief.topic | downcase }}">{{ brief.topic }}</span>
    <a href="{{ brief.url | relative_url }}">{{ brief.title }}</a>
    <span class="brief-list-date">{{ brief.date | date: "%B %Y" }}</span>
  </li>
{% endfor %}
</ul>
