  {% for post in site.posts %}
    <div>
    <article class="post">

      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1><br>
      
      </article>
      </div>
  {% endfor %}
