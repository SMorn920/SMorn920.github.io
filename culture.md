---
layout: page
title: 帷幕里外
permalink: /culture/
---

*书影音记录。*

---

{% assign entries = site.posts | where_exp: "post", "post.categories contains '书影音'" %}

{% for post in entries %}
- [{{ post.title }}]({{ post.url | relative_url }}) · {{ post.date | date: "%Y.%m.%d" }}
{% endfor %}
