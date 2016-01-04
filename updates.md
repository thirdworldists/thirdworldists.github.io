---
layout: page
title: Updates
tagline: Organisational statements and updates
description: 
---

{::nomarkdown}

{% for post in site.posts %}
{% include article_widget %}
{% endfor %}

<center>
	<a class="btn btn-default" href="{{ site.paths.atom }}">Atom Feed <span class="glyphicon glyphicon-th-list"></span></a>
	
	<a class="btn btn-default" href="http://revolutionary-aim.tumblr.com/">Tumblr blog <span class="glyphicon glyphicon-globe"></span></a>
</center>

{:/nomarkdown}
