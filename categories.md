---
layout: single
title: ""
permalink: /categories/
author_profile: false
---

<h1 style="margin-bottom:60px;">RESEARCH ARCHIVE</h1>

{% assign sorted_categories = site.categories | sort %}

{% for category in sorted_categories %}
  {% assign category_name = category[0] %}
  {% assign posts = category[1] %}

  <section style="margin-bottom:80px;">

    <h2 style="font-size:24px; letter-spacing:1px; font-weight:700; border-bottom:1px solid #111; padding-bottom:12px;">
      {{ category_name | upcase }}
    </h2>

    <ul style="list-style:none; padding-left:0; margin-top:25px;">
      {% for post in posts %}
        <li style="margin:18px 0;">
          <a href="{{ post.url | relative_url }}" style="font-size:18px; font-weight:600;">
            {{ post.title }}
          </a>
          <div style="font-size:13px; color:#666;">
            {{ post.date | date: "%B %d, %Y" }}
          </div>
        </li>
      {% endfor %}
    </ul>

  </section>

{% endfor %}
