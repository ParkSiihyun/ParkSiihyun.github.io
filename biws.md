---
layout: single
title: ""
permalink: /biws/
author_profile: false
---

<div class="sh-page-hero">
  <div class="sh-page-hero__eyebrow">BIWS Training</div>
  <h1 class="sh-page-hero__title">Breaking Into Wall Street</h1>
  <p class="sh-page-hero__lede">
    Technical financial modeling notes — from accounting fundamentals to
    DCF, LBO, M&amp;A models, and the mechanics behind each.
  </p>
</div>

{% assign biws_posts = site.categories.biws | default: site.categories.BIWS %}

{% if biws_posts %}
  <ul class="sh-post-list">
    {% for post in biws_posts %}
      <li class="sh-post-list__item">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <div class="sh-post-date">{{ post.date | date: "%B %d, %Y" }}</div>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p style="color:#5b6478;"><em>New BIWS notes coming soon.</em></p>
{% endif %}
