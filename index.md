---
layout: default
title: Home
---

<section class="hero">
  <h1>Test Blog</h1>
  <p>A clean starter site powered by Jekyll and deployed through GitHub Pages.</p>
</section>

<section>
  <h2>Latest posts</h2>

  <ul class="post-list">
    {% for post in site.posts %}
      <li class="post-card">
        <p class="post-date">{{ post.date | date: "%d/%m/%Y" }}</p>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
      </li>
    {% endfor %}
  </ul>
</section>
