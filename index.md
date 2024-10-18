---
layout: page
title: "SML"
permalink: /
---

## Building information modelling (BIM) - Semantic modelling and linking (SML)

These pages provide a way to lookup and dereference the concepts of 
<a href='-/downloads#standard' class='link dim underline-hover blue'>
CEN-EN 17632</a>.

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
<h3 class='f5 db mb4'>
<a
  class="link"
  href="https://sml.ontology-viewer.com/">
  <span class='db black mb2'>Viewer</span>
  <span class='dim underline-hover brand-dark-color f3'>SML Ontology viewer</span>
</a>
</h3>
{% endfor %}

***

Hosted by Stichting CROW on request of <a href='https://standards.cencenelec.eu/dyn/www/f?p=205:7:0::::FSP_ORG_ID:1991542&cs=100E563A3950D53807585F6A443ACB202' class='link dim underline-hover blue'>CEN/TC 442	- Building Information Modelling (BIM)</a>.