---
layout: default
title: Azure
permalink: /azure/
---

<h1>Azure</h1>
<p>The latest news about Microsoft Azure: new services, AI/cloud platform updates, regions, pricing, and best practices.</p>

{% assign posts = site.azure | sort: "date" | reverse %}
{% assign grouped = posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for group in grouped %}
{% assign first_post = group.items | first %}
{% assign month_slug = first_post.date | date: "%Y-%m" %}
<h2><a href="{{ '/azure/' | append: month_slug | append: '/' | relative_url }}">{{ group.name }}</a></h2>
<ul>
{% for post in group.items %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
