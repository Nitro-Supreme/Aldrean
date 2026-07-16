---
layout: home
title: Aldrean
---

# Welcome to Aldrean

A dark fantasy novel exploring worlds beyond mortal comprehension.

## Table of Contents

{% assign chapters = site.chapters | sort: 'chapter_number' %}

<div class="toc-container">
  <ol>
    {% for chapter in chapters %}
      <li><a href="{{ chapter.url }}">{{ chapter.title }}</a></li>
    {% endfor %}
  </ol>
</div>

---

*Select a chapter above to begin reading.*