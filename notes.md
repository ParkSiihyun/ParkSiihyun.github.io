---
layout: single
title: ""
permalink: /notes/
author_profile: false
---

<div class="sh-page-hero">
  <div class="sh-page-hero__eyebrow">Research Notes</div>
  <h1 class="sh-page-hero__title">General Notes</h1>
  <p class="sh-page-hero__lede">
    Shorter-form research notes, reading excerpts, and working ideas that
    don't yet fit cleanly into a larger case study or course.
  </p>
</div>

{% assign notes_posts = site.categories.notes | default: site.categories.Notes %}

{% if notes_posts %}
  <ul class="sh-post-list">
    {% for post in notes_posts %}
      <li class="sh-post-list__item">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <div class="sh-post-date">{{ post.date | date: "%B %d, %Y" }}</div>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p style="color:#5b6478;"><em>New notes coming soon.</em></p>
{% endif %}
