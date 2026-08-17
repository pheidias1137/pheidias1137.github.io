---
permalink: /
layout: default
---

<div class="profile">

  <img class="profile-photo" src="/assets/imgs/profile.jpg" alt="Mihica Khare">

  <div class="social-links">
    <a href="https://github.com/pheidias1137">GitHub</a>
    <a href="https://www.linkedin.com/in/mihica-khare-440079312/">LinkedIn</a>
  </div>

  <div class="intro">
    <p>
      hello, this is mihica
    </p>

    <p>
      I write & opine about tech and other things which I find interesting
    </p>
  </div>

</div>

<section class="homepage-section">
  <h1>Blog</h1>

  {% if site.posts.size > 0 %}
    {% for post in site.posts limit:5 %}
      <article class="post-preview">
        <h2>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>

        <p class="post-date">
          {{ post.date | date: "%d-%m-%Y" }}
        </p>

        {% if post.excerpt %}
          <p>{{ post.excerpt }}</p>
        {% endif %}
      </article>
    {% endfor %}
  {% else %}
    <p>Nothing here yet. Check back soon.</p>
  {% endif %}
</section>
