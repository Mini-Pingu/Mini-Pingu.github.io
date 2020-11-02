---
title: /todo
layout: page
permalink: /todo
---

**Day:**
<ol>
{% for todo_hash in site.data.todo%}
{% assign todo = todo_hash[1] %}
  <li>
    [{{ todo.date }}]: <br/>
    <ul>
    {% for task in todo.todo %}
        {% if task.priority == "high" %}
        <li><b>{{ task.title }}</b></li>
        <li><b>{{ task.description }}</b></li>
        <li><b>{{ task.priority }}</b></li>
        <hr/>
        {% else %}
        <li>{{ task.title }}</li>
        <li>{{ task.description }}</li>
        <li>{{ task.priority }}</li>
        <hr/>
        {% endif %}
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ol>
