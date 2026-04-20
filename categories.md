---
layout: single
title: ""
permalink: /categories/
author_profile: false
---

<div class="sh-page-hero">
  <div class="sh-page-hero__eyebrow">Index</div>
  <h1 class="sh-page-hero__title">All Categories</h1>
  <p class="sh-page-hero__lede">
    Everything on this site, grouped by topic.
  </p>
</div>

{% assign sorted_categories = site.categories | sort %}

{% for category in sorted_categories %}
  {% assign category_name = category[0] %}
  {% assign posts = category[1] %}

  <section class="sh-section" id="{{ category_name | slugify }}">
    <h2 class="sh-section__title">{{ category_name | upcase }}</h2>

    <ul class="sh-post-list">
      {% for post in posts %}
        <li class="sh-post-list__item">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <div class="sh-post-date">{{ post.date | date: "%B %d, %Y" }}</div>
        </li>
      {% endfor %}
    </ul>
  </section>
{% endfor %}
