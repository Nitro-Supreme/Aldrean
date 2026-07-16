---
layout: home
title: Aldrean
---

# Welcome to Aldrean

A dark fantasy novel exploring worlds beyond mortal comprehension.

**Begin your journey:**

[Read the Novel](#table-of-contents)

---

## About This Story

Aldrean is an epic tale of mystery, magic, and the forces that shape destinies. Navigate through carefully crafted chapters with integrated audio narration as you explore this dark fantasy world.

---

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

*Use the navigation menu to explore chapters, or select from the table of contents above.*