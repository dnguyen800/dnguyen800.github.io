---
layout: static
title: Home Automation
excerpt: A detailed breakdown of the gadgets that make up my smart home solution.
---


<!-- Home Automation Topic Boxes -->
<header class="major">
	<h1>Home Automation</h1>
</header>

Over the past year, I delved into one of my emerging interests—home automation—to see how it could improve daily life with the current technology.  The devices I previously owned—a voice assistant speaker, a Wi-Fi plug, some inexpensive cameras—were completely underwhelming to use, but I could see the potential. Maybe with a sizable investment, I could build a real smart home.

After fitting three homes with an array of sensors, tablets, speakers, lights and other gadgets, I have to admit that the small conveniences gained with home automation add up to something meaningful. I can listen to my music synchronized in every room in the house, cast a Youtube video from my phone to the TV while the mood lighting automatically kicks in, and control all my devices from a tablet. When it works, the house truly feels integrated and I feel at peace and can enjoy living in a cool space. 

__Not everything is perfect, but the solution I have is good enough to recommend for beginners.__ What you will find here is a collection of unbiased advice and recommendations on each aspect of the smart home, and an honest opinion on what smart homes are capable of with today’s technology.

<!-- Section Break -->
<hr class="minor" />

<section>
	<header class="major">
		<h2>Who is the audience?</h2>
	</header>
	<div class="posts">
		<article>
			<span class="image object" style="width: 20vw;" >
			  <img src="{{ '/assets/images/other/diy-skill.jpg' | absolute_url }}" alt="" style="width: 100%; " />
			</span>
			<h3>A DIY Skill Level</h3>
			<p>Not everyone aspires to be an electrician, and neither do I. My product recommendations are for do-it-yourself hobbyists with little to no professional experience in electrical work, but want to learn. To give an example of skill level needed, I can mount a TV on the wall but I would not wire an outlet without an electrician’s help.</p>
		</article>
		<article>
			<span class="image object" style="width: 20vw;" >
			  <img src="{{ '/assets/images/other/music.jpg' | absolute_url }}" style="width: 100%; " />
			</span>
			<h3>Music at my convenience</h3>
			<p>I wanted a way to enjoy my digitized music collection (over 200 CDs!) and stream music throughout the house — and I’m happy to report that this is easily achievable with Chromecast Built-in speakers and the multi-room audio feature. Using smart speakers meant sacrificing audio fidelity, but that was my only choice in order to stay within budget. It’s been really nostalgic to rediscover old favorite songs from the past two decades back. I love it!</p>
		</article>
		<article>
			<span class="image object" style="width: 20vw;" >
			  <img src="{{ '/assets/images/other/home-assistant.png' | absolute_url }}"  style="width: 100%; " />
			</span>
			<h3>A simple setup unless I really want a feature</h3>
			<p>I value my time and sanity, so I stuck with consumer products like those from Google and Nest. There are cons to using cloud-dependent products, but I haven’t found any comparable products that are easy to set up and access remotely. I also wanted a nice user interface to highlight the smart home capabilities, so I set up a <a href="https://www.home-assistant.io">Home Assistant instance</a> to serve as a dashboard. Man, what a time sink it turned out to be, but Home Assistant is arguably the coolest part of my smart home. </p>
		</article>

		<article>
			<span class="image object" style="width: 20vw;" >
			  <img src=" {{ '/assets/images/other/budget.jpg' | absolute_url }}" style="width: 100%; " />
			  </span>
			<h3>A Reasonable Budget</h3>
			<p>I favor reliability over cheaper prices, especially if it means saving time and headaches. Starting with a budget of $1,000 is enough to cover the infrastructure purchases and a few aspects of the smart home. $3,000 should be enough to cover everything except extravagant items like the Google Home Max, and iPads.</p>
		</article>
	</div>
</section>

<!-- Section Break -->
<hr class="minor" />

<header class="major">
	<h2>How easy was it to set up everything?</h2>
</header>

It wasn’t easy integrating products made by so many different vendors, but the process is much more doable today than it was  years ago. The problem with technology is that it advances so quickly, and it is inevitable that some products are no longer be supported. 

If you worry about your products becoming outdated, you will never start building your smart home, so don’t worry about it!

<hr class="minor" />

<!-- Home Automation Categories -->

<section>
	<a href="/category/Infrastructure">
      <header class="major">
	   <h2>Infrastructure</h2>
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

<section>
	<a href="/category/Media">
	<header class="major">
		<h2>Media</h2>
	</header></a>
<div class="posts">
{% for post in site.categories['Media'] %}
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

<section>
	<a href="/category/Security"><header class="major">
		<h2>Security</h2>
	</header></a>
<div class="posts">
{% for post in site.categories['Security'] %}
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

<section>
	<a href="/category/Lighting"><header class="major">
		<h2>Lighting</h2>
	</header></a>
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

<section>
	<a href="/category/Gadgets"><header class="major">
		<h2>Gadgets</h2>
	</header></a>
<div class="posts">
{% for post in site.categories['Gadgets'] %}
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

