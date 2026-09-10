---
layout: default
title: Azure
permalink: /azure/
---

<h1>Azure</h1>
<p>The latest news about Microsoft Azure: new services, AI/cloud platform updates, regions, pricing, and best practices.</p>

{% assign posts = site.azure | sort: "date" | reverse %}
{% assign current_month = "" %}
{% for post in posts %}
  {% assign this_month = post.date | date: "%B %Y" %}
  {% if this_month != current_month %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2>{{ this_month }}</h2>
    <ul>
    {% assign current_month = this_month %}
  {% endif %}
  <li>
    <span>{{ post.date | date: "%m/%d/%Y" }}</span> —
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
