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
  <!-- LEFT COLUMN -->
  <div class="card">
    <h2 class="section-title">About</h2>
    <p class="muted">
      I’m interested in investing and applied analytics — using data to make better decisions and communicate ideas clearly.
      I’ve worked in wealth management and I’m involved in student organizations on campus.
    </p>

    <hr class="hr" />

    <h2 class="section-title">Quick Links</h2>
    <p class="prose">
      <strong>Resume:</strong> <a href="{{ site.baseurl }}/resume/">View my resume</a><br/>
      <strong>Blog:</strong> <a href="{{ site.baseurl }}/blog/">Read posts</a><br/>
      <strong>Email:</strong> <a href="mailto:fjpavano@wm.edu">fjpavano@wm.edu</a><br/>
      <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/francesco-pavano" target="_blank" rel="noreferrer">francesco-pavano</a><br/>
      <strong>GitHub:</strong> <a href="https://github.com/fjpavano" target="_blank" rel="noreferrer">fjpavano</a>
    </p>
  </div>

  <!-- RIGHT COLUMN -->
  <div class="card">
    <h2 class="section-title">Featured Post</h2>

    {% assign latest = site.posts.first %}
    {% if latest %}
      <a class="featured" href="{{ site.baseurl }}{{ latest.url }}">
        <img
          class="featured__img"
          src="{{ site.baseurl }}/assets/img/featured.jpg"
          alt="Featured blog post image"
          loading="lazy"
        />
        <div class="featured__meta">
          <div class="featured__title">{{ latest.title }}</div>
          <div class="muted">{{ latest.date | date: "%b %d, %Y" }}</div>
          <p class="featured__excerpt muted">
            {{ latest.excerpt | strip_html | truncate: 220 }}
          </p>
          <div class="featured__cta">Read the post →</div>
        </div>
      </a>
    {% else %}
      <p class="muted">No posts yet.</p>
    {% endif %}
  </div>
</section>
