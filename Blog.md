---
title: Blog
layout: default
nav_order: 6
---

Excerpts of recent blog posts by category:

<!--
<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ site.url }}{{ site.baseurl }}{{ post.category }}{{ post.url }}">{{ post.title }}</a></h2>
      Excerpt: {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.url }}{{ site.baseurl }}{{ post.category }}{{ post.url }}">{{ post.title }}</a>
  {{ post.excerpt }} ...
    </li>
  {% endfor %}
</ul>
-->

<ul>
{% for category in site.categories %}
  <li><a name="{{ category | first }}">{{ category | first }}</a>
    <ul>
    {% for post in category.last %}
      <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.category }}{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%-d %B %Y" }}){{ post.excerpt }} </li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>
