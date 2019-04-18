---
title: Infrastructure
layout: static
tag: infrastructure
---
<header class="major">
	   <h1>{{ page.title }}</h1>
</header>

There are several major decisions to be made before you begin purchasing any smart device for your home. I believe choosing the appropriate network router, home automation hub, smart home wireless standard, and voice assistant is necessary for a reliable smart home. Skipping these decisions will only cause more pain later when you learn that the devices you purchased don’t integrate well or start failing for unknown reasons.

No one understands my needs better than me so I ended up buying every type of hardware until I found the right products. Doing this “research” cost me some change, so I hope you can make use of my recommendations. 

<hr class="minor" />

<!-- Home Automation Categories -->

<section>
	<a href="/category/{{ page.title }}">
      <header class="major">
	   <h2>{{ page.title }} Categories</h2>
	  </header>
	</a>
<div class="posts">
{% for post in site.categories['Infrastructure'] %}
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