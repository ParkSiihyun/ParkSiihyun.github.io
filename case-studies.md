---
layout: single
title: ""
permalink: /case-studies/
author_profile: false
---

<div class="sh-page-hero">
  <div class="sh-page-hero__eyebrow">Case Studies</div>
  <h1 class="sh-page-hero__title">Weekly Case Studies</h1>
  <p class="sh-page-hero__lede">
    Deep dives on real transactions — M&amp;A, IPOs, and capital raises —
    told through the lens of how the deal was valued, structured, and announced.
  </p>
</div>

{% assign cs_posts = site.categories["case-studies"] | default: site.categories.casestudies %}

{% if cs_posts %}
  <ul class="sh-post-list">
    {% for post in cs_posts %}
      <li class="sh-post-list__item">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <div class="sh-post-date">{{ post.date | date: "%B %d, %Y" }}</div>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p style="color:#5b6478;"><em>New case studies coming soon.</em></p>
{% endif %}
