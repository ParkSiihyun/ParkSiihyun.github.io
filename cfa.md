---
layout: single
title: ""
permalink: /cfa/
author_profile: false
---

<div class="sh-page-hero">
  <div class="sh-page-hero__eyebrow">CFA Program</div>
  <h1 class="sh-page-hero__title">CFA Study Notes</h1>
  <p class="sh-page-hero__lede">
    Structured notes following the CFA Program curriculum — Financial Statement Analysis,
    Equity, Fixed Income, Portfolio Management, and beyond.
  </p>
</div>

{% assign cfa_posts = site.categories.cfa | default: site.categories.CFA %}

{% if cfa_posts %}
  <ul class="sh-post-list">
    {% for post in cfa_posts %}
      <li class="sh-post-list__item">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <div class="sh-post-date">{{ post.date | date: "%B %d, %Y" }}</div>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p style="color:#5b6478;"><em>New CFA notes coming soon.</em></p>
{% endif %}
