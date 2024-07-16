---
layout: page
title: "SML"
permalink: /
---

## Building information modelling (BIM) - Semantic modelling and linking (SML)

These pages provide a way to lookup and dereference the concepts of 
<a href='-/downloads#standard' class='link dim underline-hover blue'>
CEN-EN 176322</a>.

***

{% assign pp = site.pages | sort: "sortkey" %}
{% for p in pp %}

{% unless p.url == page.url %}
{% unless p.dont_render %}
{% if p.title %}
<h3 class='f5 db mb4'>
<a
  class="link"
  href="{{ site.baseurl }}{{p.url | remove: '.html'}}">
  <span class='db black mb2'>{{p.title}}</span>
  <span class='dim underline-hover brand-dark-color f3'>{{p.excerpt}}</span>
</a>
</h3>

{% endif %}
{% endunless %}
{% endunless %}

{% endfor %}

***

Hosted by Stichting CROW
