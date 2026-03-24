---
layout: default
---

<header>
  <h1>Duc Anh Security Blog</h1>
  <p class="subtitle">DFIR | SOC | Threat Hunting | Malware Analysis</p>
</header>

<section class="about">
  <h2>About</h2>
  <p>Blue Team / SOC Engineer focused on Digital Forensics & Incident Response (DFIR), malware analysis, threat hunting, and detection engineering. Sharing practical writeups, lab exercises, and real-world investigations.</p>
</section>

<section class="posts">
  <h2>Latest Posts</h2>
  <ul class="post-list">
    {% for post in site.posts limit: 6 %}
    <li class="post-card">
      <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
      {% if post.tags %}
        <div class="tags">
          {% for tag in post.tags %}
            <span class="tag">#{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</section>

<section class="categories">
  <h2>Categories</h2>
  <ul>
    <li><a href="#">Malware Analysis</a></li>
    <li><a href="#">DFIR</a></li>
    <li><a href="#">Log Analysis</a></li>
    <li><a href="#">Incident Response</a></li>
    <li><a href="#">Threat Hunting</a></li>
  </ul>
</section>

<footer>
  <p>Built with ❤️ for the Blue Team • <a href="https://github.com/yourusername/your-repo" target="_blank">GitHub</a></p>
  <blockquote>"Detection is a data problem. Response is a people problem." — Unknown</blockquote>
</footer>
