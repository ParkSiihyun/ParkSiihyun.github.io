---
layout: single
title: "BIWS"
permalink: /biws/
author_profile: false
---

<h1 style="margin-bottom:50px;">BIWS TECHNICAL TRAINING</h1>

{% for post in site.categories.biws %}
  <div style="margin:25px 0;">
    <a href="{{ post.url | relative_url }}" style="font-size:18px; font-weight:600;">
      {{ post.title }}
    </a>
    <div style="font-size:13px; color:#777;">
      {{ post.date | date: "%B %d, %Y" }}
    </div>
  </div>
{% endfor %}
