---
layout: page
title: Program
permalink: /program
order: 2
---

{% assign sessions = site.data.sessions %}
{% assign program = site.data.program %}
{% assign papers = site.data.papers %}

<h1>Tentative program</h1>

<div>
{% for session in sessions %}
	{% assign sessionprogram = program | where_exp: "program", "program.session == session.session" | sort:"order" %}
	<h3>{{session.session}} Session</h3>
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