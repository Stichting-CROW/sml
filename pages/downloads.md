---
layout: page
title: Downloads
permalink: /-/downloads/
excerpt: Linked Data files and downloads
sortkey: 999
---

## Linked data files

{% assign norm1 = site.data.downloads | where: "norminform", "normative" | sort: "sortkey" | first %}
{% assign info1 = site.data.downloads | where: "norminform", "informative" | sort: "sortkey" | first %}
{% assign ex1 = site.data.downloads | where: "norminform", "example" | sort: "sortkey" | first %}

The usage of different files and ontologies is described in
<a href='#standard' class='link dim underline-hover blue'>
CEN-EN 17632</a>.
This page provides:

- <a href="{{ '#' | append: norm1.anchorid }}" class='link dim underline-hover blue b'>
{{ site.data.downloads | where: "norminform", "normative" | size }}
normative files</a>, that form the base of the CEN-EN 17632.

- <a href="{{ '#' | append: info1.anchorid }}" class='link dim underline-hover blue b'>
{{ site.data.downloads | where: "norminform", "informative" | size }}
informative files</a>, that combine the normative files for convenience.

- <a href="{{ '#' | append: ex1.anchorid }}" class='link dim underline-hover blue b'>
{{ site.data.downloads | where: "norminform", "informative" | size }}
example files</a>, that demonstrate usage.

<div class='flex-ns justify-around flex-wrap'>

<style>
.card:target {
  background: #eaf3ff;
}
@media screen and (min-width: 30em) {
  .card {
    max-width: calc( 50% - 1rem );
  }
}
</style>

{% assign files = site.data.downloads | sort_natural: "sortkey" %}
{% for download in files %}

<div
  class='flex flex-column justify-between
         br3 ph4 pv2 bg-brand-light-color mv3 mr2 dib card'
  id="{{ download.anchorid }}">
    <h3>{{ download.title }}
    <span class='gray'>— {{ download.norminform }}</span>
</h3>
<p class='f5'>
  {{ download.desc }}
  <dl class='f6'>
{% if download.namespace %}
  <dd class="b pt1 ma0">Defines in Namespace</dd>
    <dt class='pt1 pl2'><code>{{ download.namespace }}</code></dt>
{% endif %}
{% if download.ontology %}
  <dd class="b pt1 ma0">Get at URL</dd>
    <dt class='pt1 pl2'><code>{{ download.ontology }}</code></dt>
{% endif %}
{% if download.type %}
  <dd class="b pt1 ma0">Ontology Type</dd>
    <dt class='pt1 pl2'><code>{{ download.type }}</code></dt>
{% endif %}
  </dl>
</p>

<div class='center'>
  <a
    class='f6 fw6 dib ba mb3
          b--black-20 bg-brand-dark-color hover-bg-brand-middark-color white
          ph3 ph4-ns pv2 pv3-ns br2 no-underline'
    href='{{ site.baseurl }}{{ download.url }}'
    type='{{ download.mime }}'>
      <span class=''>Get</span>
      <span class=''>{{ download.url | split: "/" | last }}</span>
  </a>
</div>

</div>
{% endfor %}

</div>

---

## Standard

The standard CEN-EN 17632-1 is available at
<a href='https://standards.cencenelec.eu/dyn/www/f?p=205:110:0::::FSP_PROJECT:67839&cs=13BE091B11208910B30E53F9215AFDE96' class='link dim underline-hover blue'>
standard</a>.

The standard CEN-EN 17632-2 is under editorial ballot. It is expected to be <a href='https://standards.cencenelec.eu/dyn/www/f?p=205:110:0::::FSP_PROJECT,FSP_LANG_ID:76161,25&cs=11215E63F6DE6FE1E70AC6A77194B4E63' class='link dim underline-hover blue'>
to be published</a> in autumn 2024.



---

Hosting and Publication website provided by
<a href='https://crow.nl' class='link dim underline-hover blue'>
CROW</a>.

<div class='f7'>

This site was last generated at <code class="dim brand-dark-color">{{ site.time | date_to_xmlschema }}</code>.

</div>
