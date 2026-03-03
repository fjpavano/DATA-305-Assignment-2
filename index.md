---
layout: default
title: Home
---

<section class="card hero">
  <h1>Hi, I’m Francesco Pavano.</h1>
  <p>
    I’m a William & Mary student studying Finance (Innovation & Entrepreneurship concentration) with a minor in Data Science.
    This site is my GitHub Pages hub for my resume and short write-ups.
  </p>

  <div class="badges" aria-label="Quick highlights">
    <span class="badge">Finance</span>
    <span class="badge">Entrepreneurship</span>
    <span class="badge">Data Science</span>
    <span class="badge">Excel</span>
    <span class="badge">Python</span>
    <span class="badge">R</span>
  </div>
</section>

<section class="grid">
  <div class="card">
    <h2 class="section-title">About</h2>
    <p class="muted">
      I’m interested in investing and applied analytics — using data to make better decisions and communicate ideas clearly.
      I’ve worked in wealth management and I’m involved in student organizations on campus.
    </p>

    <hr class="hr" />

    <h2 class="section-title">What you’ll find here</h2>
    <ul class="prose">
      <li><a href="{{ site.baseurl }}/resume/">Resume</a> — education, experience, leadership, and skills</li>
      <li><a href="{{ site.baseurl }}/blog/">Blog</a> — short posts (including notes from building this site)</li>
    </ul>
  </div>

  <div class="card">
    <h2 class="section-title">Quick Links</h2>
    <p class="prose">
      <strong>Email:</strong> <a href="mailto:fjpavano@wm.edu">fjpavano@wm.edu</a><br/>
      <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/francesco-pavano" target="_blank" rel="noreferrer">francesco-pavano</a><br/>
      <strong>GitHub:</strong> <a href="https://github.com/fjpavano" target="_blank" rel="noreferrer">fjpavano</a>
    </p>

    <hr class="hr" />

    <h2 class="section-title">Currently</h2>
    <ul class="prose">
      <li>Building this Jekyll site for DATA 305</li>
      <li>Developing stronger portfolio + data workflows (Excel/Python/R)</li>
      <li>Looking for ways to apply analytics in finance</li>
    </ul>
  </div>
</section>

<section class="card" style="margin-top:16px;">
  <h2 class="section-title">Featured Post</h2>
  {% assign latest = site.posts.first %}
  {% if latest %}
    <p class="prose">
      <a href="{{ site.baseurl }}{{ latest.url }}"><strong>{{ latest.title }}</strong></a>
      <span class="muted"> — {{ latest.date | date: "%b %d, %Y" }}</span>
    </p>
    <p class="muted">{{ latest.excerpt | strip_html | truncate: 160 }}</p>
  {% else %}
    <p class="muted">No posts yet.</p>
  {% endif %}
</section>
