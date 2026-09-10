---
layout: default
title: Copilot Studio — May 2026
permalink: /copilot-studio/2026-05/
---

<p><a href="{{ '/copilot-studio/' | relative_url }}">&larr; Back to Copilot Studio</a></p>

<h1>Copilot Studio — May 2026</h1>

<ul>
{% assign posts = site.copilot-studio | where_exp: "post", "post.date | date: '%Y-%m' == '2026-05'" %}
{% assign posts = posts | sort: "date" | reverse %}
{% for post in posts %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
