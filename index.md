---
layout: home
title: Aldrean
---

# Welcome to Aldrean

A dark fantasy novel exploring a world trapped by something greater than humanity can comprehend.

## Table of Contents

{% assign chapters = site.chapters | sort: "chapter_number" %}
{% assign current_part = 0 %}

<div class="toc-container">

{% for chapter in chapters %}

  {% if chapter.part != current_part %}

    {% if current_part != 0 %}
      </ul>
    {% endif %}

    {% assign current_part = chapter.part %}

    {% assign part_name = "" %}
    {% case current_part %}
      {% when 1 %}
        {% assign part_name = "The Seal Beneath" %}
      {% when 2 %}
        {% assign part_name = "The Devourer's Debt" %}
      {% when 3 %}
        {% assign part_name = "Kethyr's Hollow" %}
      {% when 4 %}
        {% assign part_name = "The Last Dawn of Aldrean" %}
    {% endcase %}

    <h2 class="part-heading">
      Part {{ current_part }}
      <span class="part-name"> - <em>{{ part_name }}</em></span>
    </h2>

    <ul class="chapter-list">

  {% endif %}

  <li>
    <a href="{{ chapter.url | relative_url }}">
      {{ chapter.title }}
    </a>

    {% if chapter.subtitle %}
      -
      <a href="{{ chapter.url | relative_url }}" class="chapter-subtitle">
        <em>{{ chapter.subtitle }}</em>
      </a>
    {% endif %}
  </li>

{% endfor %}

</ul>

</div>

---

*Select a chapter above to begin reading.*
