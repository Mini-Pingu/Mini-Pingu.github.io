---
title: /posts
layout: page
permalink: /posts
---

<center><b>這裏會是記錄 something big 和周報。</b></center>

<hr/>

<ul>
  {% for post in site.posts %}
  <li>
    [ {{ post.date | date: "%Y-%m-%d" }} ]
    <a href="{{ post.url | relative_url }}"> {{ post.title | escape }} </a>
  </li>
  {% endfor %}
</ul>
