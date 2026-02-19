---
layout: single
title: ""
permalink: /case-studies/
author_profile: false
---

<h1 style="margin-bottom:60px;">WEEKLY CASE STUDIES</h1>

{% for post in site.categories["Case Studies"] %}
  <div style="margin:25px 0;">
    <a href="{{ post.url | relative_url }}" style="font-size:18px; font-weight:600;">
      {{ post.title }}
    </a>
    <div style="font-size:13px; color:#666;">
      {{ post.date | date: "%B %d, %Y" }}
    </div>
  </div>
{% endfor %}
