---
layout: default
title: Copilot Studio
permalink: /copilot-studio/
---

<h1>Copilot Studio</h1>
<p>News about Microsoft Copilot Studio: new agent types, connectors, orchestration features, and enterprise use cases.</p>

{% assign posts = site.copilot-studio | sort: "date" | reverse %}
{% assign grouped = posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for group in grouped %}
{% assign month_slug = group.items[0].date | date: "%Y-%m" %}
<h2><a href="{{ '/copilot-studio/' | append: month_slug | append: '/' | relative_url }}">{{ group.name }}</a></h2>
<ul>
{% for post in group.items %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
