---
layout: default
title: Home
---

# 🧠 Security Research & Writeups

> DFIR | Malware Analysis | Threat Hunting

---

{% raw %}
<div class="grid">
{% for post in site.posts %}
  <div class="card">

    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>

    <div class="meta">
      <span>{{ post.date | date: "%Y-%m-%d" }}</span>
    </div>

    <p>{{ post.excerpt }}</p>

    {% if post.tags %}
    <div class="tag-list">
      {% for tag in post.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    {% endif %}

  </div>
{% endfor %}
</div>
{% endraw %}
