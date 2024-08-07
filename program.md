---
layout: page
title: Program
permalink: /program
order: 2
---

{% assign papers = site.data.papers | sort:"title" %}

<h1>Accepted papers</h1>

<ul>
{% for paper in papers %}
    {% assign title = paper.title %}
    {% assign authors = paper.authors %}
    <li><i>{{ title }}</i> by {{ authors }}</li>
{% endfor %}
</ul>
