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

  <div class="badges" aria-label="Contact links">
    <a class="badge" href="mailto:fjpavano@wm.edu">Email</a>
    <a class="badge" href="https://www.linkedin.com/in/francesco-pavano" target="_blank" rel="noreferrer">LinkedIn</a>
    <a class="badge" href="https://github.com/fjpavano" target="_blank" rel="noreferrer">GitHub</a>
  </div>
</section>

<section class="grid">
  <!-- LEFT COLUMN -->
  <div class="card">
    <h2 class="section-title">What I’m focused on</h2>
    <ul class="prose">
      <li><strong>Finance + investing:</strong> building a stronger foundation in markets, portfolio thinking, and risk.</li>
      <li><strong>Applied analytics:</strong> using Excel, Python, and R to turn messy data into clear decisions.</li>
      <li><strong>Communication:</strong> writing and presenting ideas in a way that’s simple and convincing.</li>
    </ul>

    <hr class="hr" />

    <h2 class="section-title">Outside the classroom</h2>
    <ul class="prose">
      <li><strong>Club Soccer A (Treasurer):</strong> managing team budget and logistics.</li>
      <li><strong>Delta Chi (Philanthropy Chair):</strong> planning fundraising events and execution.</li>
      <li><strong>Golf + fitness:</strong> always chasing better performance and consistency.</li>
    </ul>

    <hr class="hr" />

    <p class="muted">
      Want the full details? See my <a href="{{ site.baseurl }}/resume/">resume</a>.
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
