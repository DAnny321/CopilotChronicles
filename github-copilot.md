---
layout: default
title: GitHub Copilot
permalink: /github-copilot/
---

<h1>GitHub Copilot</h1>
<p>News about GitHub Copilot: new features, model updates, and editor/workflow integrations.</p>

{% assign posts = site.github-copilot | sort: "date" | reverse %}
{% assign grouped = posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for group in grouped %}
<h2>{{ group.name }}</h2>
<ul>
{% for post in group.items %}
<li><span>{{ post.date | date: "%m/%d/%Y" }}</span> — <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
