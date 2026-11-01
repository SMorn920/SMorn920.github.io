---
layout: page
title: 盈虚有数
permalink: /clinical/
---

*临床手记。*

---

{% assign entries = site.posts | where_exp: "post", "post.categories contains '临床'" %}

{% for post in entries %}
- [{{ post.title }}]({{ post.url | relative_url }}) · {{ post.date | date: "%Y.%m.%d" }}
{% endfor %}
