---
layout: default
title: Home
---

## Welcome!

{{ site.description }}

---

## Recent Posts

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt | strip_html | normalize_whitespace | truncatewords: 50 }}</p>
      <a href="{{ post.url | relative_url }}">Read More »</a>
    </li>
  {% endfor %}
</ul>

<p><a href="/archive">View All Posts</a></p> <!-- Optional: Link to an archive page -->
