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

{% case current_part %}
  {% when 1 %}
    <h2 class="part-heading">Part 1 - <em>The Seal Beneath</em></h2>

  {% when 2 %}
    <h2 class="part-heading">Part 2 - <em>The Devourer's Debt</em></h2>

  {% when 3 %}
    <h2 class="part-heading">Part 3 - <em>Kethyr's Hollow</em></h2>

  {% when 4 %}
    <h2 class="part-heading">Part 4 - <em>The Last Dawn of Aldrean</em></h2>
{% endcase %}

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
