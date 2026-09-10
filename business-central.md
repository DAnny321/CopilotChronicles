---
layout: default
title: Business Central Copilot
permalink: /business-central/
---

<h1>Business Central Copilot</h1>
<p>News about Copilot features in Microsoft Dynamics 365 Business Central: new AI features, automatic categorization, AL development assistants, and more.</p>

{% assign posts = site.business-central | sort: "date" | reverse %}
{% assign grouped = posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for group in grouped %}
{% assign month_slug = group.items[0].date | date: "%Y-%m" %}
<h2><a href="{{ '/business-central/' | append: month_slug | append: '/' | relative_url }}">{{ group.name }}</a></h2>
<ul>
{% for post in group.items %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
