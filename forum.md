---
layout: page
title: Forum
---

# Forum

Здесь будут сообщения.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      — {{ post.date | date: "%Y-%m-%d" }}
    </li>
  {% endfor %}
</ul>
<form action="https://api.staticman.net/v3/entry/github/SSD-unix/forum/main/comments" method="POST">
  <input name="name" placeholder="Your name" required><br>
  <textarea name="message" placeholder="Your message" required></textarea><br>
  <button type="submit">Send</button>
</form>
<h2>Messages:</h2>
<ul>
{% for msg in site.data.messages %}
  <li>
    <b>{{ msg[1].name }}</b>: {{ msg[1].message }}
  </li>
{% endfor %}
</ul>
