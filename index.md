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

    {% case current_part %}
      {% when 1 %}
        <h2 class="part-heading">
          <span class="part-number">Part 1</span>
          <span class="part-divider"> - </span>
          <span class="part-name"><em>The Seal Beneath</em></span>
        </h2>

      {% when 2 %}
        <h2 class="part-heading">
          <span class="part-number">Part 2</span>
          <span class="part-divider"> - </span>
          <span class="part-name"><em>The Devourer's Debt</em></span>
        </h2>

      {% when 3 %}
        <h2 class="part-heading">
          <span class="part-number">Part 3</span>
          <span class="part-divider"> - </span>
          <span class="part-name"><em>Kethyr's Hollow</em></span>
        </h2>

      {% when 4 %}
        <h2 class="part-heading">
          <span class="part-number">Part 4</span>
          <span class="part-divider"> - </span>
          <span class="part-name"><em>The Last Dawn of Aldrean</em></span>
        </h2>
    {% endcase %}

    <ul class="chapter-list">

  {% endif %}
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
