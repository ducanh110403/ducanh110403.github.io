---
layout: default
title: Home
---

# 🛡️ Duc Anh Security Blog

> DFIR | SOC | Threat Hunting | Malware Analysis

---

## 👨‍💻 About Me

Xin chào, mình là **SOC / Blue Team Engineer**.  
Blog này dùng để ghi lại:

- 🔍 Malware Analysis
- 🧪 DFIR Lab
- 🚨 Incident Response
- 🧠 Threat Hunting

---

## 📚 Latest Posts

{% raw %}
{% for post in site.posts %}
<div style="margin-bottom: 20px; padding: 15px; border: 1px solid #ddd; border-radius: 10px;">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <small>{{ post.date | date: "%Y-%m-%d" }}</small>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}
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

---

## ⚡ Quote

> “Logs never lie — analysts just need to ask the right questions.”
