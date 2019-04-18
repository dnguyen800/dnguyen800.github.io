---
title: Music
layout: static
tag: music
permalink: "/category/music"
---

<!-- Home Automation Categories -->

<section>
	<a href="{{ site.baseurl }}/category/{{ page.title }}">
      <header class="major">
	   <h2>{{ page.title }} Categories</h2>
	  </header>
	</a>
<div class="posts">
{% for post in site.categories['Music'] %}
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