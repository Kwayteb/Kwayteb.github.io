---
layout: page
title: Topics
permalink: /topics/
wide: true
---

# Topics

Browse every article by subject.

<h2 id="sharia-law">Sharia Law</h2>

{% assign sharia_posts = site.categories["sharia-law"] %}
{% if sharia_posts.size > 0 %}
<ul class="article-list">
{% for post in sharia_posts %}
  <li>
    <p class="article-meta"><time>{{ post.date | date: "%b %-d, %Y" }}</time></p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 28 }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<p class="empty">No articles in this topic yet.</p>
{% endif %}

<h2 id="state-law">Formal State Law</h2>

{% assign state_posts = site.categories["state-law"] %}
{% if state_posts.size > 0 %}
<ul class="article-list">
{% for post in state_posts %}
  <li>
    <p class="article-meta"><time>{{ post.date | date: "%b %-d, %Y" }}</time></p>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 28 }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<p class="empty">No articles in this topic yet.</p>
{% endif %}
