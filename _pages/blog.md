---
layout: default
title: Blog
permalink: /blog/
---

<div class="page">
  <h1>Blog</h1>
</div>

<div class="posts">
  {% for post in site.posts %}
    <article class="post">
      <a href="{{ site.baseurl }}{{ post.url }}">
        <h1>{{ post.title }}</h1>
      </a>
      
      <p class="post_date">{{ post.date | date: "%B %e, %Y" }}</p>
      
      {% if post.img %}
      <a href="{{ site.baseurl }}{{ post.url }}">
        <img src="{{ site.baseurl }}{{ post.img }}" alt="{{ post.title }}" loading="lazy">
      </a>
      {% endif %}
      
      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More →</a>
    </article>
  {% endfor %}
</div>

{% if site.posts.size == 0 %}
<div style="text-align: center; padding: 4rem 0;">
  <p style="color: #555555; font-size: 1.1rem;">No posts yet. Check back soon!</p>
</div>
{% endif %}
