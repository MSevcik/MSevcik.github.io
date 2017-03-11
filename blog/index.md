---
layout: default
---
<div class="container-fluid jumbotron">
<div class="container">
	<h1>Blog</h1>
</div>
</div>
{% for post in site.posts %}
{% assign loopcount = forloop.index %}
<div class="container">
	<div class="row">
		<div class="col-md-10"><a style="color: black" href="{{post.url}}"><ins><h2><em>{{post.title}}</em> {% if loopcount == 1 %}<small style="color:red;"><sup><em>NEW</em></sup></small>{% endif %}</h2></ins></a></div>
		<div class="col-md-2"><h2><small>{{post.date | date_to_string}}</small></h2></div>
	</div>
	<div style="height: 2px;background-color: #b7b7b7;border-radius:5px;opacity:0.5"></div>
	<p style="margin: 10px;font-size:20px">
		{{ post.content | strip_html | truncatewords:100 }}
	</p>
	{% capture time %}{{ post.content | reading_time }}{% endcapture %}
	<h3 style="margin: 10px;">Dĺžka článku (v minútach): {{ time }}</h3>
	<div style="height: 2px;background-color: #b7b7b7;border-radius:5px;opacity:0.5"></div>
</div>
{% endfor %}