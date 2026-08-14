---
layout: default
title: Alerts
permalink: /alerts/
---
## Alerts

<ul class="brief-list">
{% assign all_alerts = site.pages | where_exp: "p", "p.path contains '/alerts/'" | where_exp: "p", "p.title != nil" | sort: 'date' | reverse %}
{% for alert in all_alerts %}
  <li>
    <span class="tag tag-alert">{{ alert.directive }}</span>
    <a href="{{ alert.url | relative_url }}">{{ alert.title }}</a>
    <span class="brief-list-date">{{ alert.date | date: "%d %b %Y" }}</span>
  </li>
{% endfor %}
</ul>
