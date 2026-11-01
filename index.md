---
layout: default
---

<div class="garden-home">
<section class="garden-intro" aria-labelledby="garden-title">
<p class="garden-kicker">A QUIET PLACE TO GROW</p>
<svg class="garden-sprig" viewBox="0 0 160 220" fill="none" stroke="currentColor" stroke-width="1.5" aria-hidden="true"><path d="M70 210 Q65 120 100 16 M78 155 Q22 145 30 99 Q76 101 78 155 M86 115 Q139 111 139 64 Q94 71 86 115 M95 69 Q57 61 65 27 Q96 34 95 69"/></svg>
<h1 id="garden-title">欢迎来到我的秘密花园</h1>
<p class="garden-subtitle">{{ site.description | escape }}</p>
<p class="garden-note">这里记录文学、音乐与电影，<br>以及那些值得慢慢想明白的事情。</p>
</section>
<nav class="garden-paths" aria-label="探索花园">
<a href="{{ '/journal/' | relative_url }}"><span class="path-number">01 / JOURNAL</span><h2>白驹过隙</h2><p>思绪万千，且行且感。</p><span aria-hidden="true">走进随笔 →</span></a>
<a href="{{ '/culture/' | relative_url }}"><span class="path-number">02 / CULTURE</span><h2>帷幕里外</h2><p>在书页、旋律与光影间停留。</p><span aria-hidden="true">翻阅书影音 →</span></a>
<a href="{{ '/clinical/' | relative_url }}"><span class="path-number">03 / CLINICAL</span><h2>盈虚有数</h2><p>临床手记，记录观察与思考。</p><span aria-hidden="true">阅读手记 →</span></a>
</nav>
<section class="garden-recent" aria-labelledby="recent-title">
<div class="garden-section-head"><h2 id="recent-title">新近落笔</h2><span>RECENT ENTRIES</span></div>
<ul class="garden-posts">
{% for post in site.posts limit:6 %}
<li><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y.%m.%d" }}</time><div><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>{% if site.show_excerpts %}<div class="garden-excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</div>{% endif %}</div></li>
{% else %}<li>种子已经埋下，文字会慢慢生长。</li>{% endfor %}
</ul>
<a class="garden-feed" href="{{ '/feed.xml' | relative_url }}">订阅花园 · RSS ↗</a>
</section>
<p class="garden-closing">愿这里的一切，都能慢慢生长。</p>
</div>
