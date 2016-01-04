---
layout: index
title: Revolutionary Anti-Imperialist Movement
tagline: 
description: 
---

## What is RAIM?

{% include what_is_raim %}

## Latest Updates

{% for post in site.posts limit:3 %}
{% include article_widget %}
{% endfor %}

<center>
	<a class="btn btn-default" href="{{ site.paths.updates }}">More updates <span class="glyphicon glyphicon-bullhorn"></span></a>

	<a class="btn btn-default" href="http://revolutionary-aim.tumblr.com/">Tumblr blog <span class="glyphicon glyphicon-globe"></span></a>
</center>
