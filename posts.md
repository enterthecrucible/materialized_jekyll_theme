---
layout: page
title: "Blog"
---

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <h2>
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    <div class="chip"><span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span></div>
    </h2>
    <div class="entry-content">{{ post.excerpt }}</div>
  </li>
  <div class="divider"></div>
  {% endfor %}
  </ul>
