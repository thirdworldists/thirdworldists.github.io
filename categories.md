---
layout: page
title: Categories
tagline: 
description: Post Categories List
---

{::nomarkdown}
{% for category in site.categories %} 
	<h3 id="{{ category[0] }}">{{ category[0] | join: "/" }}</h3>
	<ul>
		{% assign list_pages = category[1] %}  
		{% include list_pages %}
	</ul>
{% endfor %}
{:/nomarkdown}
