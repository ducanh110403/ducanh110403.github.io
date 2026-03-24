---
layout: default
title: Home
---

# 🚀 Duc Anh Blog

## 📚 Bài viết

{% raw %}
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endraw %}
