{% assign paper = papers | where_exp: "p", "p.paperid == talk.paperid" | first %}
{% assign start = talk.start %}
{% assign end = talk.end %}
{% assign title = paper.title %}
{% assign authors = paper.authors %}
{% if talk.url %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i><a href="{{talk.url}}">{{ title }}</a>a</i> by {{ authors }}</li>
{% else %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i> by {{ authors }}</li>
{% endif %}
