---
layout: default
---

<!-- Hobbies -->

<section>
	<header class="major">
		<h2>Topics</h2>
	</header>
	<div class="features">
		<article>
			<span class="icon fa-home"></span>
			<div class="content">
				<h3><a href="{{ '/category/Home%20Automation' | absolute_url }}">Home Automation</a></h3>
				<p>I wanted to see what was possible with home automation in 2019, so I tested some exciting new technologies you may not have realized are available today.</p>
			</div>
		</article>
		<article>
			<span class="icon fa-globe"></span>
			<div class="content">
				<h3><a href="{{ 'category/Travel' | absolute_url }}">Travel</a></h3>
				<p>I was fortunate enough to take time off and travel around parts of the world. I have some routes and tips to share for those who are planning their  next long-term adventure.</p>
			</div>		  
		</article>
		<article>
			<span class="icon fa-camera-retro"></span>
			<div class="content">
				<h3><a href="{{ 'works.html' | absolute_url }}">Photography</a></h3>
				<p>I'm not a photographer, but I took a few nice photos during my travels. Here is a curated selection of said photos.</p>
			</div>		  
		</article>
	</div>
</section>

<!--  -->
<!-- Latest Updates -->

<section>
	<header class="major">
		<h2>Latest Updates</h2>
	</header>
	<div class="posts">
	{% for post in site.posts limit:3 %}
		<article>
			<div class="article-image" style='background-image: url("{{ site.baseurl }}/assets/images/grid-ws2/{{ post.short_title }}.jpg");'>
				<div class="overlay"><a href="{{ site.baseurl }}{{ post.url }}">
					<h2>{{ post.title }}</h2></a>
				</div>
			</div>
			<p>{{ post.update }}</p>
		</article>
    {% endfor %}	
	</div>
</section>

