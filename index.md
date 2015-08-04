---
layout: page
title: Janto's Blog!
tagline: Code is life
---
{% include JB/setup %}

{% for post in site.posts %}
  <h2> <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
  ****
  <p>{{post.content}}</p>
  <ul>
    {% assign categories_list = post.categories %}  
    {% include JB/categories_list %}
  </ul>
  <p><span>{{ post.date | date: "%B %e, %Y" }}</span></p>
  ----
{% endfor %}
