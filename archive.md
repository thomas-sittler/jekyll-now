---
layout: page
permalink: /all/
title: all posts
---

<div class="posts">
  {% for post in site.posts %}
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><br><br>
  {% endfor %}
</div>
