{% assign paper = papers | where_exp: "p", "p.paperid == talk.paperid" | first %}
{% assign start = talk.start %}
{% assign end = talk.end %}
{% assign title = paper.title %}
{% assign authors = paper.authors %}
<li>{{start}}-{{end}}&nbsp;&nbsp;<i>{{ title }}</i> by {{ authors }}</li>