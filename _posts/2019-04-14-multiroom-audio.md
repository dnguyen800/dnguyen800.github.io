---
layout: page
title: Multi-room Audio
short_title: multiroom-audio
excerpt: Previously a wired-only and costly solution, multi-room audio is now available for music lovers with modest budgets.
permalink: /multiroom-audio
competitors: "Google Home/Chromecast, Amazon Echo, Sonos One, Apple Homepod, Denon Heos, and wired solutions"
image: assets/images/overlay-ws/multiroom-audio.jpg
image_credit: Dan Nguyen
categories: 
    - "Music"
    - "Media"
    - "Home Automation"
---


#### I’ve personally tested the following:

| ![Google Home](assets\images\logo\chromecast.png){:.image.logo} | ![Amazon Echo photo](assets\images\logo\amazon.png){:.image.logo} |
|:-------:|:--------:|
| **Google Home**<br>**Insignia Speaker with Google Assistant** | **Amazon Echo (1st gen)**<br>**Echo Dot (2nd gen)** |

## What you need to know

Multi-room audio is the ability to play music synchronized with speakers placed around the house to achieve the effect of music following you around the house. It works really well and is one of my favorite uses in a smart home.  By using the Wi-Fi network that is already in your house, it is possible to connect wireless smart speakers together~. I'm not sure why it took so long to get it working, but I'm glad I can now have this feature in a rented apartment or house. 

App support can be very limited, depending on what company you choose. At the very least, Spotify is supported on all multi-room audio formats.


### Considerations before choosing multi-room audio speakers

<ul class="alt">
	<li><b>Research app compatibility with multi-room audio before buying.</b> Chromecast supports the most services. Amazon Echo and Sonos doesn’t support Plex for local music.</li>
</ul>

### What you get with multi-room audio speakers


<ul class="alt">
	<li>Synchronized music in every room.</li>
	<li>Continue the music playing from your car to the house.</li>
	<li>Start playing multi-room music using your voice or music app.</li>
	<li>Depending on your choice, works with most major music apps.</li>	
</ul>


### Recommended Reading

<ul class="alt">
	<li>Purchase the <a href="https://www.bestbuy.com/site/insignia-voice-smart-portable-bluetooth-speaker-and-alarm-clock-with-google-assistant-gray-black/5865906.p?skuId=5865906">Insignia Large speaker with Google Assistant</a></li>
	<li>Slickdeals.net sales of the <a href="https://slickdeals.net/newsearch.php?searchin=first&forumchoice%5B%5D=9&forumchoice%5B%5D=44&forumchoice%5B%5D=25&forumchoice%5B%5D=30&q=insignia+speaker+google+assistant&r=1">Insignia speakers</a></li>
	<li>Wirecutter review of the <a href="https://thewirecutter.com/reviews/best-soundbar/#budget-pick-vizio-sb3651-e6">Vizio Smartcast Soundbar</a></li>
</ul>

<!-- Product Review section -->
<hr class="major" />

## Chromecast Built-in Speakers

![Chromecast Built-in](assets\images\logo\chromecast-builtin.png){:.image.dan-left}

**With a wide selection of reasonably priced compatible AV receivers, speakers and soundbars to choose from, I recommend using any highly rated Chromecast built-in speaker in your home.** If you already have a good pair of speakers, then connect a Chromecast Audio (discontinued as of Jan 2019) to it. There are so many combinations of Chromecasts you can use—even the Chromecast TV dongles work with multi-room audio now, allowing you to leverage your existing TV, receiver and soundbars.  Any speaker that supports Chromecast Built-in will have the same easy setup experience and compatibility with apps that support Chromecast. 

The main selling point of Chromecast is the number of apps that support it. Where else can you find multi-room audio support for a nearly dead music service like SoundCloud? Chromecast is the only solution I’ve found that can stream multi-room audio from Plex for local music. Last I checked, Amazon Echo and Sonos support Plex but for individual speakers only.


### The Problems

I’ve found Chromecast to be a more frustrating user experience than Amazon Echo—music playback can take a few seconds to start, or not start at all until I force close and re-open the Spotify app. When you're performing a lot of actions in a short period of time (for example, trying to stop and restart playback of a video because of an error), it only makes things worse. This issue happens on both iOS and Android Spotify and Youtube apps quite often, so I think it is a problem Chromecast itself. Luckily, I haven't had any troubles getting music to play using voice control.

Is that the price to pay for compatibility? Unfortunately, yes. I’m able to live with that trade-off for more supported music apps, but it is one of the biggest annoyances with this setup.  


### Installation and Smart Home Integration

After setting up  the speakers in the Google Home app, create a speaker group in the Google Home app and that’s it--you can access your speaker group in Spotify, Plex, or anything else that supports Chromecast speakers.

<figure class="align-center">
 <img src="assets\images\other\chromecast-setup.png" />
 <figcaption>
The Chromecast/Google Home setup process.
 </figcaption>
</figure>

Home Assistant detects individual Chromecast speakers and speaker groups if the ``Discovery`` component is enabled. I use the ``Universal Media Player component`` to combine all speakers and groups into one Home Assistant entity and show the music currently playing. 

One small quirk I found is that if you want send a broadcast message to all speakers using Home Assistant, you must use a Home Assistant group, not a Google group. As long as you are not constantly renaming your speakers in Google Home, this shouldn't be a problem. 

Voice control with Google Assistant works great with Spotify. Mention the name of the speaker group and Google will play music there.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/chromecast-ha.png" />
        <figcaption>
          <b>Home Assistant: Great</b><br>  Autodetects speakers and displays media info like so.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <b>Voice: Great</b><br> Say "Hey Google, play Spotify on "speaker group" and it works.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/chromecast-spotify.png"  />
      <figcaption>
      <b>Spotify: Okay</b><br> Sometimes need to force close the app to work.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/chromecast-app.png"  />
       <figcaption>
         <b>Native App: Good</b><br> Control settings, volume and media playback from the app.
       </figcaption>
      </figure>
	</div>
</div>

<br>
<!-- Product Review section -->
<hr class="minor" />

<div class="row">
  <div class="12u 12u$(small)">
      <figure class="align-left">
       <img src="assets\images\product-photo\insignia-speaker.png" alt=""/>
       <figcaption>
         The large version of the Insignia speaker. <b>|  Best Buy</b>
       </figcaption>
       </figure>
	  <h2>Insignia Large Speaker with Google Assistant</h2>
      <p><b>For those who want multi-room audio without breaking the bank, the Insignia Large Speaker with Google Assistant from Best Buy is a good value when it goes on sale for $35.</b>  It sounds slightly better than the Google Home speakers, and has a few nifty features like a battery that lasts for three hours, and a LED display to show the time and temperature. I was able to outfit my home with these speakers for under $200! This is more of a brag than recommendation since the sale is over, but do check Slickdeals periodically if it appears again. There is one big problem with these speakers, which I will go into detail below.
      </p>
<h3>The Problems</h3>
<p>I’ve tested these speakers thoroughly for months now, and they’re great, except for one significant issue. The sound cuts off when playing low-sounding music — it’s especially noticeable on classical, piano, or acoustic songs. The problem fades away by increasing the volume, but listening to classical volume at high volume is a bit of an oxymoron. Firmware updates haven’t resolved the issue yet in the past year, so it’s likely to be a hardware issue that may never be resolved. That is unfortunate because I am a big fan of these speakers.
</p>
<p>Another wish I have for this speaker is an auxiliary input jack. I wanted to connect my Nintendo Switch, laptop and desktop computer audio to the speaker but that is not possible with Chromecast technology. Bluetooth technically works but the audio delay is noticeable, and the quality is not good enough for me.</p>
  </div>
</div>

<!-- Product Review section -->
<hr class="minor" />

<div class="row">
	<div class="12u 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\vizio-soundbar.jpg" alt=""/>
        <figcaption>
          Vizio's entry-level 2.1 sound bar. <b>|  Vizio</b>
        </figcaption>
        </figure>
		<h2>Vizio Smartcast Sound Bar</h2>
		<p><b>For Chromecast Built-in sound bars, the Vizio Smartcast sound bars are considered the best value.</b> <a href="(https://thewirecutter.com/reviews/best-soundbar/#budget-pick-vizio-sb3651-e6">The Wirecutter</a> recommends them for the best mix of performance, connectivity, features, and price in the budget category. The problems I had with the Insignia speakers are fixed here--there is support for auxiliary (3.5mm, headphone jack, whatever you call it) inputs, optical, analog, and HDMI, so every device can be hooked up to it. I personally have not tested this sound bar, but I have tried previous versions of Vizio sound bars and I was always happy with the value.</p>

<p>I tested another soundbar, the <a href="https://www.amazon.com/Polk-Audio-MagniFi-Theater-System/dp/B01LW76AKC/ref=sr_1_3?ie=UTF8&qid=1546626122&sr=8-3&keywords=polk+magnifi+mini">Polk Magnifi Mini</a>, and found the Chromecast integration working as expected, but the trade-off of sound quality for the smaller size and price was not worth it. For the cost of the Mini (a 2.1 set), you could get the Vizio 5.1 sound bar set.</p>
  </div>
</div>

<!-- Product Review section -->
<hr class="major" />

## The Competition

<div class="row">
	<div class="6u 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\sonos-one.jpg" alt=""/>
        <figcaption>
          The Sonos One. <b>|  Sonos</b>
        </figcaption>
        </figure>
		<h3>Sonos</h3>
		<p>I don’t own any Sonos products because I’m happy (for now) with my cheap Chromecast Built-in speakers, but if I were willing to spend over $1,000 then I would look into getting Sonos One speakers and a sound bar for my setup. The sound quality is likely better than Chromecast speakers and Amazon Echo, though the voice assistant function is either bad or non-existent. Check out Amazon reviews to get an idea of the complaints. I'm going to assume that Sonos makes a good speaker but a terrible voice assistant, which that may be acceptable to those who don’t want a speaker listening in at all times.</p>
	</div>
	<div class="6u$ 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\amazon-echo-1st.jpg" alt=""/>
        <figcaption>
          The Amazon Echo. <b>|  Amazon</b>
        </figcaption>
        </figure>
		<h3>Amazon Echo</h3>
		<p>I think Amazon Echo's multi-room music feature is much more reliable than Chromecast, but it only works with a few services: Spotify, Amazon Music Unlimited, TuneIn, iHeartRadio and Pandora. Support for Spotify took some time to complete--support was announced on August 2017, but wasn't rolled out until December 2017.  Another downside to Amazon's implementation is that Amazon Echo speakers are locked to one Amazon & Spotify account and don't allow casting from guests.  When I visited my friend's house, I couldn't cast music from my phone to the Echo speaker because of this issue. Voice control works, but I prefer having more options.  

Amazon's multi-room audio solution doesn't support Plex for local music, so I couldn't use it with my solution. </p>
  </div>
</div>