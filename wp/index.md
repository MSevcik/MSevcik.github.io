---
layout: projects
dataanchor: wp
title: Webové publikovanie
sub: Zadania
desc: Na tejto stránke budem postupne zverejňovať zadania z predmetu webové publikovanie.
---
{% for project in site.data.projects[page.dataanchor] %}
<div>
	<h3>{{project.name}}</h3>
	<p style="font-size: 18px">{{project.desc}}</p>
	<a style="margin-top: 5px" class="btn btn-primary" href="{{project.link}}">Otvoriť</a>
</div>
{% endfor %}

