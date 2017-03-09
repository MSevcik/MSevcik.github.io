---
layout: blog
---
<div class="container">
	{% for post in site.posts offset:1%}
		<div style="border-radius:5px;margin: 5px;border-color: #dddddd;border-width: 2px;border-style: solid;" class="row">
			<div class="col-md-2">
				<h4>{{post.title}}</h4>
			</div>
			<div class="col-md-8">
				<p>{{post.content | strip_html | truncatewords: 50}}</p>
			</div>
			<div class="col-md-2">
				<a style="width: cover;" class="btn btn-primary center" href="{{post.url}}">Čítaj viac</a>
			</div>
		</div>
	{% endfor %}
</div>