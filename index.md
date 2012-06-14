---
layout: page
title: TDD in der Realität
tagline: 
---
{% include JB/setup %}

## Blog


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date: "%d.%m.%Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>




## Katalog der Standard-Situationen

TODO

<a class="btn btn-success btn-large btn-primary" href="katalog.html"><i class="icon-book icon-white"> </i> Zum Katalog</a>
