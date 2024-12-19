{% assign start = talk.start %}
{% assign end = talk.end %}
{% assign title = talk.title %}
{% assign presenter = talk.presenter %}

{% if talk.url %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i><a href="{{talk.url}}">{{ title }}</a></i>{% if presenter %} by {{ presenter }}{% endif %}</li>
{% else %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i>{% if presenter %} by {{ presenter }}{% endif %}</li>
{% endif %}
