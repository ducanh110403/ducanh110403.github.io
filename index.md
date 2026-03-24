---
layout: default
title: Home
---

# 🛡️ Duc Anh Security Blog

> DFIR | SOC | Threat Hunting | Malware Analysis

---

## 👨‍💻 About

Blue Team / SOC Engineer focusing on:

- Malware Analysis  
- Digital Forensics (DFIR)  
- Threat Hunting  
- Incident Response  

---

## 📚 Latest Posts

{% raw %}
<div class="post-list">
{% for post in site.posts %}
  <div class="post-card">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <small>{{ post.date | date: "%Y-%m-%d" }}</small>
    <p>{{ post.excerpt }}</p>
  </div>
{% endfor %}
</div>
{% endraw %}

---

## 🧩 Categories

- 🦠 Malware Analysis  
- 🔐 DFIR  
- 📊 Log Analysis  
- 🚨 Incident Response  

---

## 📫 Contact

- GitHub: https://github.com/ducanh110403
