---
layout: single
title: "Research & Study Archive"
permalink: /categories/
author_profile: false
---

{% assign sorted_categories = site.categories | sort %}

{% for category in sorted_categories %}
  {% assign category_name = category[0] %}
  {% assign posts = category[1] %}

  <h2 style="margin-top:60px; border-bottom:2px solid #111; padding-bottom:10px;">
    {{ category_name | upcase }}
  </h2>

  <ul style="list-style:none; padding-left:0;">
    {% for post in posts %}
      <li style="margin:20px 0;">
        <a href="{{ post.url | relative_url }}" style="font-size:20px; font-weight:600;">
          {{ post.title }}
        </a>
        <div style="font-size:14px; color:#666;">
          {{ post.date | date: "%B %d, %Y" }}
        </div>
      </li>
    {% endfor %}
  </ul>

{% endfor %}
