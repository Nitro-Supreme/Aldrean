---
layout: home
title: Aldrean
---

# Welcome to Aldrean

A dark fantasy novel exploring a world trapped by something greater than humanity can comprehend.

## Table of Contents

{% assign chapters = site.chapters | sort: 'chapter_number' %}
{% assign current_part = 0 %}

<div class="toc-container">
  {% for chapter in chapters %}
    {% if chapter.part != current_part %}
      {% if current_part != 0 %}</ul>{% endif %}
      <h3 class="part-heading">## Part {{ chapter.part }}</h3>
      <ul>
      {% assign current_part = chapter.part %}
    {% endif %}
    <li>
      <a href="{{ chapter.url | relative_url }}">{{ chapter.title }}</a>
      {% if chapter.subtitle %}<span class="chapter-subtitle">— {{ chapter.subtitle }}</span>{% endif %}
    </li>
  {% endfor %}
  </ul>
</div>

---

*Select a chapter above to begin reading.*
