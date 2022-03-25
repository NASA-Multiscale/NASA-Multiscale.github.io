---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

Welcome to the NASA Multiscale Community Site.

The purpose of this site are to:

-   Provide documentation of the NASA Multiscale Analysis Tool
	(NASMAT) and related computational methods.
-   Be a community resource for use and enhancement of multiscale methods


### Recent news
<ul>
  {% for post in site.posts limit:10 %}
    <li>
      <a href="{{ site.url }}{{ site.baseurl }}{{ post.category }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
