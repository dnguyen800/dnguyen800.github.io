---
title: Security
short_title: security
layout: static
tag: security
permalink: "/category/security"
---

<!-- Home Automation Topic Boxes -->
<header class="major">
	<h1>Security</h1>
</header>

It has taken a long time for home security to come into the (really) affordable mainstream, but with the advent of reliable wireless technology in smart locks, cameras and security systems and with healthy competition, now is a good time to start looking into home security options. Renters should also consider adding home security, since the latest solutions are wireless and can be relocated. 

There are three approaches to security you can take, depending on your needs.

**Do-it-yourself.** For people who don’t need professional 24/7 monitoring, but want a little visibility into their household’s safety, then installing a few cameras will do the job. There will always be a delay in response — the same as the time it takes for you to respond to a phone notification. 

**Self Installation with Professional monitoring.** The introduction of wireless sensors brought down the cost of security systems to a reasonable price, so there isn’t much reason NOT to go with this route. You can always opt-out of monitoring and keep as a self-monitoring solution as well.

**Professional everything.** Traditional security system and monitoring services are still available to rip you off, much like cable TV. If you don’t mind spending more money and want a completely hassle-free installation and solution, then Frontpoint Security is a good option.

<hr class="minor" />

<!-- Home Automation Categories -->


<section>
	<a href="{{ site.baseurl }}/category/{{ page.title }}">
      <header class="major">
	   <h2>{{ page.title }} Categories</h2>
	  </header>
	</a>
<div class="posts">
{% for post in site.categories['Security'] %}
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