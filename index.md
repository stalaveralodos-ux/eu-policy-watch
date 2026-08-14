---
layout: page
title: EU Policy Watch
permalink: /briefs/
---

## What is the Commission doing now?

A running log of the legislative files shaping Brussels in 2026, tracked as they move through Parliament and Council.

The Commission's 2026 Work Programme sets out 47 legislative initiatives, with simplification as the central thread: more than half carry a strong simplification component, building on the omnibus approach already used for sustainability reporting and now extended to digital rules, energy product legislation, taxation and citizens' rules. Alongside simplification, the programme leans into competitiveness (following the Draghi report), defence readiness by 2030, and a comprehensive push on migration and returns.

This page tracks the files worth watching, one brief at a time: where each stands, what is at stake for those affected, and what to watch next.

### Briefs

{% assign sorted_briefs = site.briefs | sort: 'date' | reverse %}
{% for brief in sorted_briefs %}
- **[{{ brief.title }}]({{ brief.url }})** — {{ brief.date | date: "%B %Y" }}
{% endfor %}
