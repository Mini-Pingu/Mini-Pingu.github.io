---
title: /posts
layout: page
permalink: /posts
---

# Posts

<ul class="entries">
  {% for post in site.posts %}
  <li>
    [{{ post.date | date: "%d %B %Y" }}]
    <a href="{{ post.url }}">
    	{{ post.title }}
    </a>
  </li>
  {% endfor %}
</ul>
