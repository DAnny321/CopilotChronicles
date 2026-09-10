---
layout: default
title: GitHub Copilot
permalink: /github-copilot/
---

<h1>GitHub Copilot</h1>
<p>News about GitHub Copilot: new features, model updates, and editor/workflow integrations.</p>

{% assign posts = site.github-copilot | sort: "date" | reverse %}
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
