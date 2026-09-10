---
layout: default
title: Microsoft 365 Copilot
permalink: /m365-copilot/
---

<h1>Microsoft 365 Copilot</h1>
<p>News about Microsoft 365 Copilot: new features in Word, Excel, Outlook, Teams, and the other apps in the suite.</p>

{% assign posts = site.m365-copilot | sort: "date" | reverse %}
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
