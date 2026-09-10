---
layout: default
title: GitHub Copilot — September 2026
permalink: /github-copilot/2026-09/
---

<p><a href="{{ '/github-copilot/' | relative_url }}">&larr; Back to GitHub Copilot</a></p>

<h1>GitHub Copilot — September 2026</h1>

<ul>
{% assign posts = site.github-copilot | where_exp: "post", "post.date | date: '%Y-%m' == '2026-09'" %}
{% assign posts = posts | sort: "date" | reverse %}
{% for post in posts %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
