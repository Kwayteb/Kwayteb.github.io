---
layout: page
title: Home
permalink: /
wide: true
---

# Common Ground

A place to read and discuss writing on Sharia law and formal state law — side by side, in plain language.

## Browse by topic

<div class="topic-grid">
  <a class="topic-card" href="{{ '/topics/' | relative_url }}#sharia-law">
    <h3>Sharia Law</h3>
    <p>Commentary and explainers on Islamic jurisprudence.</p>
  </a>
  <a class="topic-card" href="{{ '/topics/' | relative_url }}#state-law">
    <h3>Formal State Law</h3>
    <p>Writing on statutory and constitutional law.</p>
  </a>
</div>

## Recent articles

<ul class="article-list">
{% for post in site.posts limit:6 %}
  <li>
    <p class="article-meta">
      <time>{{ post.date | date: "%b %-d, %Y" }}</time>
      {% if post.categories contains "sharia-law" %}<span class="pill">Sharia Law</span>{% endif %}
      {% if post.categories contains "state-law" %}<span class="pill">Formal State Law</span>{% endif %}
    </p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 28 }}</p>{% endif %}
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
<p class="empty">No articles yet — add your first Markdown file to <code>_posts/</code> to see it here.</p>
{% endif %}
