---
layout: page
title: TDD in the Real World
tagline: 
---
{% include JB/setup %}

You can find on this site the materials from a tutorial about "TDD in the Real
World", given by the four of us at the 2012 [_Entwicklertag_ conference in
Karlsruhe](http://entwicklertag.de).

For this tutorial, we have developed a new approach to coaching TDD as a _skill
and habit_, rather than just as a technique and tool. Along with the materials,
we also explain some of the background in our [blog](blog/index.html).



### Materials from the tutorial

<a class="btn btn-success btn-large btn-primary" 
href="https://github.com/downloads/andrena/reality-tdd/en-KatalogDerStandardsituationen.pdf">
<i class="icon-book icon-white"> </i> Set-piece play (the catalog)</a>



### Blog

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date: "%d.%m.%Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
