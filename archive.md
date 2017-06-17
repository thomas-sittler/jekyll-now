---
layout: page
permalink: /all/
tite: all posts
---

<div class="posts">
  {% for post in site.posts %}
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
  {% endfor %}
</div>
