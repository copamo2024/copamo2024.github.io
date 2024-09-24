{% assign paper = papers | where_exp: "p", "p.paperid == talk.paperid" | first %}
{% assign start = talk.start %}
{% assign end = talk.end %}
{% assign title = paper.title %}
{% assign authors = paper.authors %}
{% assign url = paper.url %}
{% if url %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i><a href="{{ url }}">{{ title }}</a></i> by {{ authors }}</li>
{% else %}
  <li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i> by {{ authors }}</li>
{% endif %}
