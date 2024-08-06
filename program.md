---
layout: page
title: Program
permalink: /program
order: 2
---

{% assign papers = site.data.papers %}

<h1>Program</h1>

<ul>
{% for paper in papers %}
    {% assign title = paper.title %}
    {% assign authors = paper.authors %}
    <li>{{ authors }} - <i>{{ title }}</i></li>
{% endfor %}
</ul>
