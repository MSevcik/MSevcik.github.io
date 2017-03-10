---
layout: default
---
<div style="margin-top: 70px"></div>
<div class="container">
	<h1>Blog</h1>
</div>
{% for post in site.posts %}
{% assign loopcount = forloop.index %}
---
<div class="container">
	<div class="row">
		<div class="col-md-10"><a style="color: black" href="{{post.url}}"><ins><h2><em>{{post.title}}</em> {% if loopcount == 1 %}<small style="color:red;"><sup><em>NEW</em></sup></small>{% endif %}</h2></ins></a></div>
		<div class="col-md-2"><h2><small>{{post.date | date_to_string}}</small></h2></div>
	</div>
	<div style="height: 2px;background-color: #b7b7b7;border-radius:5px;opacity:0.5"></div>
	<p style="margin: 10px;font-size:20px">
		{{ post.content | strip_html | truncatewords:100 }}
	</p>
</div>
{% endfor %}