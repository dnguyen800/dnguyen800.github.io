---
layout: static
title: Travel
excerpt: Travel
Update: <strong>April 26, 2019:</strong> The first addition to the Travel section. Some of my personal notes on travel preparations.
---

<!--more-->

<!-- Home Automation Categories -->

<section>
	<a href="/category/Travel%20Preparation">
      <header class="major">
	   <h2>Travel Preparations</h2>
	  </header>
	</a>
<div class="posts">
{% for post in site.categories['Travel Preparation'] %}
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