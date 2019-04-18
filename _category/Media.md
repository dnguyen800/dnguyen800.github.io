---
title: Media
tag: media
permalink: "/category/media"
layout: static
---

<!-- Home Automation Categories -->

<section>
	<header class="major">
		<h2>{{ page.title }} Categories</h2>
	</header>
	<div class="posts">
	{% for post in site.categories['Media'] %}
		<article>
		  <div class="article-image" style='background-image: url("{{ site.baseurl }}/assets/images/grid-ws2/{{ post.short_title }}.jpg");'>
			<div class="overlay"><a href="{{ site.baseurl }}{{ post.url }}">
			  <h2>{{ post.title }}</h2></a>
			</div>
		  </div>
	  <p>{{ post.excerpt }}</p>
	</article>
    {% endfor %}
	</div>
</section>