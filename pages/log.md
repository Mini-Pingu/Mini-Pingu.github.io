---
title: /log
layout: page
permalink: /log
---

**Day:**
<ol>
{% for log_hash in site.data.log %}
{% assign log = log_hash[1] %}
  <li>
    [{{ log.date }}]: <br/>
    <ul>
    {% for task in log.tasks %}
        <li>{{ task.title }}</li>
        <li>{{ task.description }}</li>
        <li>{{ task.status }}</li>
        <li><b>Upcoming:</b> {{ task.upcoming }}</li>
        <hr/>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ol>
