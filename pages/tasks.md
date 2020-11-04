---
title: /tasks
layout: page
permalink: /tasks
---

<center><b>這裏會是日報記錄，詳細進度可參考各 repository 的 README.md。</b></center>

<hr/>

**Day:**
<ol>
{% for tasks_hash in site.data.tasks %}
{% assign item = tasks_hash[1] %}
  <li>
    [{{ item.date }}]: <br/>
    <ul>
    {% for task in item.tasks %}
        <li><b>{{ task.title }}</b>: {{ task.info }}</li>
        <li>priority: {{ task.priority }}</li>
        <li>stage: {{ task.stage }}</li>
        <li>steps: <b>{{ task.steps }}</b></li>
        <li>current: <b>{{ task.current }}</b></li>
        <li>current_percentage: <b>{{ task.current_percentage }}</b></li>
        <li>link: <a href="{{ task.link }}">{{ task.repository }}</a></li>
        <li>parent: {{ task.parent }}</li>
        <hr/>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ol>
