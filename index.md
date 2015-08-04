---
layout: page
title: Janto's Blog!
tagline: Code is life
---
{% include JB/setup %}

{% for post in site.posts %}
  <h3>Categories for: {{ post.title }}</h3>
  <ul>
    {% assign categories_list = post.categories %}  
    {% include JB/categories_list %}
  </ul>
{% endfor %}
