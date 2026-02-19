---
layout: single
title: "CFA"
permalink: /cfa/
author_profile: false
---

<h1 style="margin-bottom:50px;">CFA PROGRAM NOTES</h1>

{% for post in site.categories.cfa %}
  <div style="margin:25px 0;">
    <a href="{{ post.url | relative_url }}" style="font-size:18px; font-weight:600;">
      {{ post.title }}
    </a>
    <div style="font-size:13px; color:#777;">
      {{ post.date | date: "%B %d, %Y" }}
    </div>
  </div>
{% endfor %}
