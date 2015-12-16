---
layout : blog
title : The Blog Of Adelowo Lanre
bloghome : true
---

  {% for post in site.posts %}
  
  <div class="col-md-4 post-grid">
    <article itemscope itemtype="http://schema.org/Article">

      <h2 itemprop="name">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      </h2>

      <div class="excerpt" itemprop="description">
        {{ post.excerpt }}
      </div>
      
      <div class="footer">
      {% if post.date %}<span class="published">
      <i class="fi-calendar"></i>  <time datetime="{{ post.date | date: "%Y-%m-%d" }}" itemprop="datePublished">{{ post.date | date: "%b %d, %Y" }}</time></span>{% endif %}
      <a href="{{ site.baseurl }}{{ post.url }}" class="button read-more">Read More</a>
      </div>
    </article>
    
    </div>
  {% endfor %}