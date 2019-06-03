---
layout: page
title: Multi-room Audio
short_title: multiroom-audio
update: "<strong>May 27, 2019:</strong> Added my review of the Sonos Play:1 speaker, which has been replaced by the Sonos One. Super confusing name, if you ask me."
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

| ![Google Home](assets\images\logo\chromecast.png){:.image.logo} | ![Amazon Echo photo](assets\images\logo\amazon.png){:.image.logo} |![Sonos](assets\images\logo\sonos.png){:.image.logo}
|:-------:|:--------:|:--------:|
| **Google Home**<br>**Insignia Speaker with Google Assistant** | **Amazon Echo (1st gen)**<br>**Echo Dot (2nd gen)** | **Sonos Play:1** |

## What you need to know

Multi-room audio is the ability to play music synchronized with speakers placed around the house to achieve the effect of music following you around the house. It works really well and is one of my favorite uses in a smart home.  By using the Wi-Fi network that is already in your house, it is possible to connect wireless smart speakers together. I'm not sure why it took so long to get the technology working, but I'm glad I can now have this feature in a rented apartment or house. 

App support for multi-room audio can be very limited, depending on what company you choose (Google, Amazon, Sonos). At least Spotify is supported on all multi-room audio formats.


### Considerations before choosing multi-room audio speakers

<ul class="alt">
	<li><strong>Research app compatibility with multi-room audio before buying.</strong> Chromecast supports the most services. Amazon Echo and Sonos doesn’t support Plex for local music.</li>
</ul>

### What you get with multi-room audio speakers

<ul class="alt">
	<li>Synchronized music in every room.</li>
	<li>Continue the music playing from your car to the house by using voice commands.</li>
	<li>Start playing multi-room music using your voice or mobile app.</li>
	<li>Depending on your choice (Google, Amazon, Sonos), multi-room audio works with most major music apps.</li>	
</ul>


### Recommended Reading

<ul class="alt">
  <li><strong>Affiliate Link:</strong> Purchase the <a href="https://amzn.to/2L8SHXt">Vizio 2.1 sound bar</a>, <a href="https://amzn.to/2XWn1Gt">Sonos One</a> or <a href="https://amzn.to/2WcI1Zf">Amazon Echo 2nd Gen</a> from Amazon</li>
  <li>Purchase the <a href="https://www.bestbuy.com/site/insignia-voice-smart-portable-bluetooth-speaker-and-alarm-clock-with-google-assistant-gray-black/5865906.p?skuId=5865906">Insignia Large speaker with Google Assistant</a></li>
  <li>Slickdeals.net sales of the <a href="https://slickdeals.net/newsearch.php?searchin=first&forumchoice%5B%5D=9&forumchoice%5B%5D=44&forumchoice%5B%5D=25&forumchoice%5B%5D=30&q=insignia+speaker+google+assistant&r=1">Insignia speakers</a></li>
  <li>Wirecutter review of the <a href="https://thewirecutter.com/reviews/best-soundbar/#budget-pick-vizio-sb3651-e6">Vizio Smartcast Soundbar</a></li>
</ul>

<!-- Product Review section -->
<hr class="major" />

## Chromecast Built-in Speakers

![Chromecast Built-in](assets\images\logo\chromecast-builtin.png){:.image.dan-left}

**With a wide selection of reasonably priced compatible AV receivers, speakers and soundbars to choose from, I recommend using any highly rated Chromecast built-in speaker in your home.** If you already have a good pair of speakers, then connect a Chromecast Audio ([discontinued](https://www.theverge.com/2019/1/11/18178751/google-chromecast-audio-discontinued-sale) as of Jan 2019) to it. There are so many combinations of Chromecasts you can use—even the Chromecast TV dongles work with multi-room audio now, allowing you to leverage your existing TV, receiver and soundbars.  Any speaker that supports **``Chromecast Built-in``** will have the same easy setup experience and compatibility with apps that support Chromecast. 

It's also very easy to let guests play music to Chromecast speakers. As long as the guests are connected to the same Wi-Fi network as the speakers, any Chromecast-supported app should detect the speakers and allow casting. The last time I checked (around January 2019), Amazon Echo speakers do not support any form of casting outside of the Amazon user who registered the Echo. You can still use voice commands to play Spotify on an Echo speaker, but you can't select a song from the Spotify app and cast to the Echo speaker.

The main selling point of Chromecast is the incredible number of apps that support it. Where else can you find multi-room audio support for a nearly dead music service like SoundCloud? Chromecast is the only solution I’ve found that can stream multi-room audio from Plex for local music. Amazon Echo and Sonos support Plex but for individual speakers only.


### The Problems

I’ve found Chromecast to be a more frustrating user experience than Amazon Echo—music playback can take several seconds to start, or not start at all until I force close and re-open the Spotify app. When you're performing a lot of actions in a short period of time (e.g. stopping and restarting a Youtube video because of an error), it only makes things worse. This issue happens on both iOS and Android Spotify and Youtube apps quite often, so I think it is a problem Chromecast itself. Luckily, I haven't had any troubles getting music to play using voice control.

I use the Spotify Windows app quite often, and unfortunately it's not possible to cast music from the app. Casting from the Spotify web player using Google Chrome works, because Chrome has casting function built into the browser.

Is that the price to pay for compatibility? Unfortunately, yes. I’m able to live with that trade-off for more supported music apps, but it is one of the biggest annoyances with this setup.  


### Installation and Smart Home Integration

After setting up  the speakers in the Google Home app, create a speaker group in the Google Home app and that’s it--you can access your speaker group in Spotify, Plex, or anything else that supports Chromecast speakers.

<figure class="align-center">
 <a class="image-link" href="assets\images\other\chromecast-setup.png" ><img src="assets\images\other\chromecast-setup.png" /></a>
 <figcaption>
The Chromecast/Google Home setup process.
 </figcaption>
</figure>

Home Assistant detects individual Chromecast speakers and speaker groups if the [**``Discovery``**](https://www.home-assistant.io/components/discovery/) component is enabled. I use the [**``Universal Media Player``**](https://www.home-assistant.io/components/universal/) component to combine all speakers and groups into one Home Assistant entity and show the music currently playing. 

One small quirk I found is that if you want send a broadcast message to all speakers using Home Assistant, you must use a Home Assistant group, not a Google group. As long as you are not constantly renaming your speakers in Google Home, this shouldn't be a problem. 

Voice control with Google Assistant works great with Spotify. Mention the name of the speaker group and Google will play music there.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/chromecast-ha.png" />
        <figcaption>
          <strong>Home Assistant: Great</strong><br>  Autodetects speakers and displays media info like so.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Great</strong><br> Say "Hey Google, play Spotify on "speaker group" and it works.
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
      <strong>Spotify: Okay</strong><br> Sometimes need to force close the app to work.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/chromecast-app.png"  />
       <figcaption>
         <strong>Native App: Good</strong><br> Control settings, volume and media playback from the app.
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
         The large version of the Insignia speaker. <strong>|  Best Buy</strong>
       </figcaption>
       </figure>
	  <h2>Insignia Large Speaker with Google Assistant</h2>
      <p><strong>For those who want multi-room audio without breaking the bank, the <a href="https://www.bestbuy.com/site/insignia-voice-smart-portable-bluetooth-speaker-and-alarm-clock-with-google-assistant-gray-black/5865906.p?skuId=5865906">Insignia Large Speaker with Google Assistant</a> from Best Buy is a good value when it goes on sale for $35.</strong>  It sounds slightly better than the Google Home speakers, and has a few nifty features like a battery that lasts for three hours, and a LED display to show the time and temperature. I was able to outfit my home with these speakers for under $200! This is more of a brag than recommendation since the sale is over, but do check <a href="https://slickdeals.net/newsearch.php?searchin=first&forumchoice%5B%5D=9&forumchoice%5B%5D=44&forumchoice%5B%5D=25&forumchoice%5B%5D=30&q=insignia+speaker+google+assistant&r=1">Slickdeals</a> periodically if it appears again. There is one big problem with these speakers, which I will go into detail below.
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
          Vizio's entry-level 2.1 sound bar. <strong>|  Vizio</strong>
        </figcaption>
        </figure>
		<h2>Vizio Smartcast Sound Bar</h2>
		<p><strong>For Chromecast Built-in sound bars, the <a href="https://amzn.to/2L8SHXt">Vizio Smartcast sound bars</a> are considered the best value.</strong> <a href="(https://thewirecutter.com/reviews/best-soundbar/#budget-pick-vizio-sb3651-e6">The Wirecutter</a> recommends them for the best mix of performance, connectivity, features, and price in the budget category. The problems I had with the Insignia speakers are fixed here--there is support for auxiliary (3.5mm, headphone jack, whatever you call it) inputs, optical, analog, and HDMI, so every device can be hooked up to it. I personally have not tested this sound bar, but I have tried previous versions of Vizio sound bars and I was always happy with the value.</p>

<p>I tested another soundbar, the <a href="https://amzn.to/2V6cxqX">Polk Magnifi Mini</a>, and found the Chromecast integration working as expected, but the trade-off of sound quality for the smaller size and price was not worth it. For the cost of the Mini (a 2.1 set), you could get the Vizio 5.1 sound bar set.</p>
  </div>
</div>


<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
  <img src="assets\images\product-photo\sonos-play1.png" alt=""/>
  <figcaption>
    The Sonos Play:1 speaker. <strong>|  Sonos</strong>
  </figcaption>
</figure>

## Sonos

I finally had the chance to test out an old pair of Sonos Play:1 speakers, which have already been replaced by the [Sonos One](https://amzn.to/2QvW36f), but the Sonos experience and integration is pretty much the same.  **After a few days of testing, I can say that there are several things that Sonos does better than Chromecast, but I found too many odd limitations that prevent me from whole heartedly recommending Sonos.** If you can live with the limitations (read below), then go for Sonos if you have the money.

Besides better sound quality, Sonos is better than Chromecast in a few ways for me. Music playback starts within three seconds, versus the ten seconds with Chromecast. Switching to different speakers just works with Sonos, whereas Chromecast may take a few attempts to get working. I also love the fact that I can use the Spotify Windows app to cast music to Sonos speakers or headphones without skipping a beat. Lastly, I believe Sonos is the only media player that is officially supported by SmartThings. It's not a big deal, but adding Sonos to SmartThings means adding text-to-speech announcements to automations, like when someone is arriving home. The same automation can be done in Home Assistant and Chromecast, but I prefer creating automations in SmartThings as it is more reliable.

<figure class="align-center" style="width: 20%">
 <a class="image-link" href="assets\images\other\sonos-spotify-windows.png" ><img src="assets\images\other\sonos-spotify-windows.png" /></a>
 <figcaption>
Sonos speakers can be selected on the Spotify Windows app.
 </figcaption>
</figure>

On January 2019, Sonos added the [ability](https://en.community.sonos.com/announcements-228985/sonos-now-playing-with-alexa-groups-6817588) to add Sonos speakers to an Alexa Group. Does this mean you can group Sonos and Amazon Echo speakers together for synchronized music? Unfortunately, I don't think that is the case. The main use of this feature is to pair an Echo Dot with a Sonos speaker in the same Alexa Group so that any voice command to play music is automatically routed to the Sonos speaker without having to mention the speaker name.

### The Problems 

The lack of a auxiliarty or RCA inputs prevents this from being my main speaker. I can't connect the speaker to my Nintendo Switch or laptop without high latency or expensive workarounds like the [Genki bluetooth adapter](https://amzn.to/2HHsETB) for Nintendo Switch. 

### More Problems / Smart Home Integration

App support is complicated. Sonos works very well with Spotify (my main [streaming music choice](streaming-media-services#spotify), but not with Plex (my main [local music choice](streaming-media-services#plex)).  I can't cast music from the Plex app to a Sonos speaker. Using the Sonos app, Plex technically works only if the Plex server is made available on the internet. My server is hosted locally, but Chromecast speakers still work with the Plex app on the local network.
		
The Sonos app wants to be the app for all music sources, but I don't recommend using it because the app disables playback control from other sources, like the Spotify app, or voice control. Spotify and Google Assistant cannot tell if music is actively playing from the Sonos speaker (if using the Sonos app) and thus cannot control music playback through those methods. There really isn't any reason to use the Sonos app, except for grouping speakers.
		
I prefer Google's approach to grouping speakers--I can add one speaker to multiple groups but still select the individual speaker for music playback. In contrast, Sonos handles speaker grouping in the worst way possible. A speaker can be added to one group only, and once a Sonos speaker is added to a group, you can no longer cast music to the individual speaker unless you remove the speaker from the group using the Sonos app. Having speaker groups like Upstairs, Downstairs, and the Whole House aren't possible without workarounds because only one speaker can be in one group. Speaker group management can be done in the Sonos app and even Home Assistant, using the [Mini Media Player](https://github.com/kalkih/mini-media-player) card.

Sonos integrates with Google Assistant, but it is not a deep integration. Voice commands are similar to Google Home, except you must mention the name of the Sonos speaker, like "play Spotify on living room." Once music is playing, you can no longer have to say the speaker name to pause or change songs. 


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/sonos-playone-ha.jpg" />        <figcaption>
          <strong>Home Assistant: Great</strong><br> Built-in integration exists, full playback control and media info like so.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Good</strong><br> Say "Hey Google, play Spotify on "speaker name" and it works. To play music to a speaker group, say the name of the master speaker.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/sonos-playone-st.png"  />
      <figcaption>
      <strong>SmartThings: Good</strong><br>Provides playback control and shows artist and song information.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/sonos-playone-app.jpg"  />
       <figcaption>
         <strong>Sonos App: Okay</strong><br> Technically works, but playing music through the Sonos app hinders voice and playback control from other apps.
       </figcaption>
      </figure>
	</div>
</div>


<!-- Product Review section -->


<hr class="major" />

## The Competition

<div class="row">
	<div class="6u$ 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\amazon-echo-1st.jpg" alt=""/>
        <figcaption>
          The Amazon Echo. <strong>|  Amazon</strong>
        </figcaption>
        </figure>
		<h3>Amazon Echo</h3>
		<p>I think <a href="https://amzn.to/2WcI1Zf">Amazon Echo's</a> multi-room music feature is much more reliable than Chromecast, but it only works with a few services: Spotify, Amazon Music Unlimited, TuneIn, iHeartRadio and Pandora. Support for Spotify took some time to complete--support was announced on August 2017, but wasn't rolled out until December 2017.  Another downside to Amazon's implementation is that Amazon Echo speakers are locked to one Amazon/Spotify account--guests cannot cast music from their phones to Amazon Echo speakers.  When I visited my friend's house, I couldn't cast music from my phone to the Echo speaker because of this issue. Voice control works to play Spotify, but then I would be potentially interrupting someone's Spotify session.</p> 

<p>Amazon's multi-room audio solution doesn't support Plex for local music, so I couldn't use it with my solution. </p>
  </div>
</div>