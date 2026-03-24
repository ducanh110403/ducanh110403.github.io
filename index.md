---
layout: default
title: Home
---

<div class="hero">
  <h1>Duc Anh Security Blog</h1>
  <p>DFIR | SOC | Threat Hunting | Malware Analysis</p>
</div>

---

## 🧠 About

Cybersecurity enthusiast focused on:

- Digital Forensics (DFIR)
- Malware Analysis
- Threat Detection & Hunting
- Incident Response

---

## 📚 Latest Research & Writeups

{% raw %}
<div class="grid">
{% for post in site.posts %}
  <div class="card">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
    <p>{{ post.excerpt }}</p>
  </div>
{% endfor %}
</div>
{% endraw %}
