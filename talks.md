---
layout: page
title: Talks
permalink: /talks
order: 3
---

{% assign sessions = site.data.sessions %}
{% assign program = site.data.program %}
{% assign papers = site.data.papers %}

<div>
{% for session in sessions %}
	{% assign sessionprogram = program | where_exp: "program", "program.session == session.session" | sort:"order" %}
	<h3>{{session.session}} Session: {{session.title}}</h3>
	<p>Chaired by <a href="{{session.chairurl}}">{{session.chair}}</a>.</p>
	<ul>
		{% for talk in sessionprogram %}
			{% if talk.paperid%}
				{% include talk.md %}
			{% else %}
				{% include other.md %}
			{% endif %}
		{% endfor %}
	</ul>
{% endfor %}
</div>
