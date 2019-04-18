---
title: Lighting
tag: lighting
layout: static
permalink: "/category/lighting"
---

<!-- Home Automation Categories -->


<section>
	<a href="/category/{{ page.title }}">
      <header class="major">
	   <h2>{{ page.title }} Categories</h2>
	  </header>
	</a>
<div class="posts">
{% for post in site.categories['Lighting'] %}
	<article>
	  <div class="article-image" style='background-image: url("/assets/images/grid-ws2/{{ post.short_title }}.jpg");'>
			<div class="overlay"><a href="{{ post.url }}">
			  <h2>{{ post.title }}</h2></a>
			</div>
	  </div>
	  <p>{{ post.excerpt }}</p>
	</article>	
{% endfor %}
</div>
</section>