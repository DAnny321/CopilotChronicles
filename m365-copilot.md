---
layout: default
title: Microsoft 365 Copilot
permalink: /m365-copilot/
---

<h1>Microsoft 365 Copilot</h1>
<p>News about Microsoft 365 Copilot: new features in Word, Excel, Outlook, Teams, and the other apps in the suite.</p>

{% assign posts = site.m365-copilot | sort: "date" | reverse %}
{% assign grouped = posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for group in grouped %}
{% assign first_post = group.items | first %}
{% assign month_slug = first_post.date | date: "%Y-%m" %}
<h2><a href="{{ '/m365-copilot/' | append: month_slug | append: '/' | relative_url }}">{{ group.name }}</a></h2>
<ul>
{% for post in group.items %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
