---
layout: default
title: Side Stories
permalink: /side-stories/
---

<div class="home-container">
  <h1>Side Stories</h1>
  <p>Shorter tales set within Aldrean, alongside the main novel.</p>
</div>

<div class="toc-container">

{% assign stories = site.side_stories | sort: "order" %}

{% if stories.size == 0 %}
  <p class="coming-soon centered">No side stories have been posted yet. Check back soon.</p>
{% else %}
  <ul class="chapter-list">
  {% for story in stories %}
    <li>
      <a href="{{ story.url | relative_url }}">{{ story.title }}</a>
      {% if story.subtitle %}
        - <a href="{{ story.url | relative_url }}" class="chapter-subtitle"><em>{{ story.subtitle }}</em></a>
      {% endif %}
    </li>
  {% endfor %}
  </ul>
{% endif %}

</div>
