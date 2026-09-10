---
layout: default
title: Home
---

<h1>CopilotChronicles</h1>
<p>Le ultime novità dal mondo Copilot, organizzate per tema: GitHub Copilot, Microsoft Copilot Studio, Microsoft 365 Copilot, Copilot per Business Central e Azure.</p>

{% assign all_posts = "" | split: "," %}
{% assign all_posts = all_posts | concat: site.github-copilot %}
{% assign all_posts = all_posts | concat: site.copilot-studio %}
{% assign all_posts = all_posts | concat: site.m365-copilot %}
{% assign all_posts = all_posts | concat: site.business-central %}
{% assign all_posts = all_posts | concat: site.azure %}
{% assign sorted_posts = all_posts | sort: "date" | reverse %}

<h2>Ultimi post</h2>
<ul>
  {% for post in sorted_posts limit: 20 %}
    <li>
      <span>{{ post.date | date: "%d/%m/%Y" }}</span> —
      <strong>[{{ post.theme_label }}]</strong>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<h2>Esplora per tema</h2>
<ul>
  <li><a href="{{ '/github-copilot/' | relative_url }}">GitHub Copilot</a></li>
  <li><a href="{{ '/copilot-studio/' | relative_url }}">Copilot Studio</a></li>
  <li><a href="{{ '/m365-copilot/' | relative_url }}">Microsoft 365 Copilot</a></li>
  <li><a href="{{ '/business-central/' | relative_url }}">Copilot per Business Central</a></li>
  <li><a href="{{ '/azure/' | relative_url }}">Azure</a></li>
</ul>
