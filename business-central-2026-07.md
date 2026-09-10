---
layout: default
title: Business Central Copilot — July 2026
permalink: /business-central/2026-07/
---

<p><a href="{{ '/business-central/' | relative_url }}">&larr; Back to Business Central Copilot</a></p>

<h1>Business Central Copilot — July 2026</h1>

<ul>
{% assign posts = site.business-central | where_exp: "post", "post.date | date: '%Y-%m' == '2026-07'" %}
{% assign posts = posts | sort: "date" | reverse %}
{% for post in posts %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
