---
layout: page
title: 白驹过隙
permalink: /journal/
---

*思绪万千，且行且感。*

---

{% assign entries = site.posts | where_exp: "post", "post.categories contains '随笔'" %}

{% for post in entries %}
- [{{ post.title }}]({{ post.url | relative_url }}) · {{ post.date | date: "%Y.%m.%d" }}
{% endfor %}
