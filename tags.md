---
layout: page
title: Tags
tagline: 
description: Post Tags List
---

{::nomarkdown}
<ul class="tag_box inline">
	{% assign list_tags = site.tags %}  
	{% include list_tags %}
</ul>

{% for tag in site.tags %} 
	<h3 id="{{ tag[0] }}">{{ tag[0] }}</h3>
	<ul>
		{% assign list_pages = tag[1] %}  
		{% include list_pages %}
	</ul>
{% endfor %}
{:/nomarkdown}
