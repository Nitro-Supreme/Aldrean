---
layout: default
title: Term Reference
permalink: /terms/
---

<div class="home-container">
  <h1>Term Reference</h1>
  <p>A glossary of places, factions, powers, and things better left buried.</p>
</div>

<div class="terms-container">

{% assign current_category = "" %}
{% assign shown_any = false %}

{% for term in site.data.terms %}
  {% if site.data.terms_visible contains term.id %}
    {% assign shown_any = true %}
    {% if term.category != current_category %}
      {% if current_category != "" %}
        </div>
      {% endif %}
      {% assign current_category = term.category %}
      <h2 class="term-category-heading">{{ current_category }}</h2>
      <div class="terms-group">
    {% endif %}
    <details class="term-entry">
      <summary>{{ term.name }}</summary>
      <p>{{ term.definition }}</p>
    </details>
  {% endif %}
{% endfor %}

{% if current_category != "" %}
  </div>
{% endif %}

{% unless shown_any %}
  <p class="coming-soon centered">No terms revealed yet. Check back soon.</p>
{% endunless %}

</div>
