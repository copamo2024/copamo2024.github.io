{% assign start = talk.start %}
{% assign end = talk.end %}
{% assign title = talk.title %}
{% assign presenter = talk.presenter %}

<li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i>
{% if talk.subtitle %}
{% if talk.url %}
<a href="{{talk.url}}">
{% endif %}
: <b>{{ talk.subtitle }}</b>
{% if talk.url %}
</a>
{% endif %}
{% else %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i>{% if presenter %} by {{ presenter }}{% endif %}</li>
{% endif %}
