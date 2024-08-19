{% assign start = talk.start %}
{% assign end = talk.end %}
{% assign title = talk.title %}
{% assign presenter = talk.presenter %}
<li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i>{% if presenter %} by {{ presenter }}{% endif %}</li>