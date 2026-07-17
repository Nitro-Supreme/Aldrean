---
layout: default
title: Characters
permalink: /characters/
---

<div class="home-container">
  <h1>Characters</h1>
  <p>The people, and the things that used to be people, moving through a world that does not remember how many times it has already ended.</p>
</div>

<div class="card-grid">
{% assign chars = site.characters | sort: "order" %}
{% for char in chars %}
  {% if site.data.characters_visible contains char.slug %}
    <a href="{{ char.url | relative_url }}" class="character-card">
      <h3>{{ char.name }}</h3>
      <p class="card-role">{{ char.role }}</p>
      <p class="card-faction">{{ char.faction }}</p>
      <p class="card-desc">{{ char.short }}</p>
    </a>
  {% endif %}
{% endfor %}
</div>

{% assign visible_count = 0 %}
{% for char in chars %}
  {% if site.data.characters_visible contains char.slug %}
    {% assign visible_count = visible_count | plus: 1 %}
  {% endif %}
{% endfor %}
{% if visible_count == 0 %}
  <p class="coming-soon centered">No characters revealed yet. Check back soon.</p>
{% endif %}
