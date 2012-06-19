---
layout: page
title: TDD in the Real World
tagline: 
---
{% include JB/setup %}

### TDD in the Real World

You can find on this site the materials from a tutorial about "TDD in the Real
World", given by the four of us at the 2012 [_Entwicklertag_ conference in
Karlsruhe](http://entwicklertag.de).

For this tutorial, we have developed a new approach to coaching TDD as a _skill
and habit_, rather than just as a technique and tool. Along with the materials,
we also explain some of the background in our [blog](blog/).


### TDD in der Realität

Auf dieser Seite findet ihr die Materialien zu einem Tutorial über "TDD in der
Realität", das wir beim [Karlsruher Entwicklertag 2012](http://entwicklertag.de)
gehalten haben.

Für dieses Tutorial haben wir einen neuen Ansatz zum Entablieren von TDD als
Fertigkeit und Angewohnheit (skill/habit) entwickelt, der über die bloße Sicht
als Technologie und Werkzeug hinausgeht. Zusätzlich zu den Materialien gibt es
auf unserem [Blog](blog/) mehr Informationen zu Hintergründen und
Details unseres Vorgehens.



## Downloads

<p>
<a class="btn" 
href="https://github.com/downloads/andrena/reality-tdd/en-KatalogDerStandardsituationen.pdf">
<i class="icon-book"> </i> Set-piece play (the catalog)</a>
<a class="btn" 
href="https://github.com/downloads/andrena/reality-tdd/de-KatalogDerStandardsituationen.pdf">
<i class="icon-book"> </i> Katalog der Standardsituationen</a>
</p>
<p>
<a class="btn" 
href="https://github.com/downloads/andrena/reality-tdd/de-Handout-pmem.pdf">
<i class="icon-eye-close"> </i> Übung zum vorausschauenden Erinnern</a>
</p>


## Blog

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date: "%d.%m.%Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<p>
<a class="btn btn-success" href="blog/">
<i class="icon-chevron-right icon-white"> </i> Read more…</a>
</p>
