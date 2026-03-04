---
layout: page
title: Blog
permalink: /blog/
---

<section class="card">
  <div class="blog-hero">
    <div class="blog-hero__text">
      <h1 class="section-title">Blog</h1>
      <p class="muted">
        Short write-ups on things I care about.
      </p>
  </div>
</section>

<section class="posts">
  {% for post in site.posts %}
    <article class="card post-card">
      <a class="post-card__link" href="{{ site.baseurl }}{{ post.url }}">
        <div class="post-card__img">
          <img
            src="{{ site.baseurl }}{{ post.image | default: '/assets/img/featured.jpg' }}"
            alt="{{ post.title }} thumbnail"
            loading="lazy"
          />
        </div>

        <div class="post-card__content">
          <div class="post-card__title">{{ post.title }}</div>
          <div class="muted">{{ post.date | date: "%b %d, %Y" }}</div>
          <p class="post-card__excerpt muted">
            {{ post.excerpt | strip_html | truncate: 160 }}
          </p>
          <div class="post-card__cta">Read →</div>
        </div>
      </a>
    </article>
  {% endfor %}
</section>
