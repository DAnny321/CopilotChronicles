---
layout: default
title: Business Central Copilot
permalink: /business-central/
---

<h1>Business Central Copilot</h1>
<p>News about Copilot features in Microsoft Dynamics 365 Business Central: new AI features, automatic categorization, AL development assistants, and more.</p>

{% assign posts = site.business-central | sort: "date" | reverse %}
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
