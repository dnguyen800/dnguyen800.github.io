---
layout: page
title: Streaming Media Devices
short_title: streaming-media-device
excerpt: The cordcutter's life isn't as simple as it used to be, but adding a device like the Roku ensures you get access to all the major streaming services.
competitors: "Google Chromecast, Amazon Fire TV, Roku, Apple TV, Android TV, smart TVs, video game consoles"
permalink: /streaming-media-device
image: assets/images/overlay-ws/streaming-media-device.jpg
image_credit: Dan Nguyen
categories: 
    - "Media"
    - "Home Theater"
    - "Home Automation"
---

<!--more-->


#### I’ve personally tested the following:

|---
| ![](assets\images\logo\chromecast.png){:.image.logo} |  ![](assets\images\logo\roku.png){:.image.logo} | ![](assets\images\logo\amazon.png){:.image.logo} | ![](assets\images\logo\apple.png){:.image.logo}
|:-:|:-:|:-:|:-:
| **Chromecast Ultra <br> Chromecast (1080p)<br>Chromecast (720p)** | **Roku Streaming Stick+<br> Roku Premiere** | **Amazon Fire TV 2 (2016)<br>Fire TV Stick (2014)** | **Apple TV 2**

## What you need to know

The new lineup of media streaming devices continues to impress every year. With more features like 4K, voice control, and HDR added into physically smaller devices, I feel like I can constantly upgrade my old TV at a cheap price. Indeed, my 2015 Vizio TV is more useful with a Roku Streaming Stick+ so I no longer have to browse through a slow, ancient web interface. 

<div class="box">
	<p><i>Though media streaming devices are capable of impressive feats, I’ve found thxat the best TV watching experience lies with a high-end smart TV like the LG OLED series.  The gyroscopic remote controls make it as easy as possible for anyone to pick up a remote and intuitively browse through the TV’s wide selection of apps. The LG OLED TVs are really impressive, if you can afford it. See the <a href="{{ 'smart-tv.html' | absolute_url }}">Smart TV Section</a> to learn more.</i></p>
</div>


### Considerations before buying a media streaming device

<ul class="alt">
  <li><strong>A media streaming device may not be necessary</strong> if your TV or video game console supports the same video apps.</li>
  <li><strong>Companies sell 1080p and 4K versions of their products.</strong> I recommend future-proofing by purchasing the 4K version.</li>
  <li><strong>Beware: When you use a media streaming device or service, your TV viewing data is being collected.</strong> There’s a reason why these devices are so cheap: the companies are collecting data on the videos you watch, and possibly selling the information to third parties, like advertisers. The Vizio CTO said so himself in this <a href="https://www.theverge.com/2019/1/7/18172397/airplay-2-homekit-vizio-tv-bill-baxter-interview-vergecast-ces-2019">podcast.</a></li>
</ul>

### What you get with a media streaming device

<ul class="alt">
  <li>Upgrade an outdated TV with new features like voice control, and a faster browsing experience.</li>
  <li>Use the Roku as a ghetto universal remote with <a href="https://www.home-assistant.io/components/emulated_roku/">emulated Roku feature</a> on Home Assistant.</li>
  <li>Integrated smart home automations, as nearly all devices are supported by Home Assistant.</li>
  <li>Move media streaming devices to different TVs.</li>
</ul>

### Recommended reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2XhNo9l">Roku Streaming Stick+</a>, or <a href="https://amzn.to/2XjoExH">Amazon Fire TV Stick 4k</a> on Amazon</li>
  <li>The Wirecutter’s Best Streaming Device <a href="https://thewirecutter.com/reviews/best-media-streamers/">Recommendation</a></li>
  <li>The <a href="https://www.home-assistant.io/components/roku/">Roku</a> and  <a href="https://www.home-assistant.io/components/emulated_roku/">Emulated Roku</a> component for Home Assistant</li>
</ul>


<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\roku-ultra.png" alt=""/>
 <figcaption>
The Roku Ultra. <strong>|  Roku</strong>
 </figcaption>
</figure>

## Roku

**I recently switched over to the Roku Streaming Stick+, and agree with the Wirecutter that it is the best media streaming device available today.** It supports both Google Assistant and Amazon Alexa, as well as Youtube TV and Amazon Prime Video—all without any workarounds. Normally when you try to be a jack of all trades, you end up being good at nothing. In this case, Roku ends up being good enough for my needs, and I haven’t found anything missing besides deeper integration with voice assistants. I just hope Google and Amazon don’t take away their respective apps from Roku and create more segregated market.

I find the Roku voice search function on the remote is much more useful with the ability to search for a title through multiple apps. I never purchase TV shows or movies, so I like Roku’s search function because it highlights the free or subscription options first. Google Assistant and Alexa are officially supported, though it is limited to opening apps, powering on TV or changing volume. Voice commands aren’t as deeply integrated at the application level, compared to the Fire TV or even the Chromecast.

On the premium Roku products like the **``Streaming Stick+``**, the remote includes extra nifty features like TV power and volume control buttons. This also works in tangent with HDMI ARC to control the AV receiver or soundbar volume. With this, I’m able to dump my old TV remote. Though it lacks an Input Change button, I have HDMI-CEC working so rarely do I need it.

### The Problems
The casting feature on Roku is supported on some apps, but not as many as Chromecast. I did a quick test and found that casting works on Netflix, Youtube, Youtube TV, but not Hulu or Plex. It seems like a weird oversight as Roku can easily cast videos as Chromecast. There are times when I miss the casting to Chromecast. So I decided—why not use both? As both devices support HDMI-CEC, I don’t have to worry about switching TV inputs. Though if I’m paying for two devices, I should consider purchasing an Android TV like the Nvidia Shield TV.

### Installation and Smart Home Integration
Roku is easily detected and automatically integrated with Home Assistant as a media player and remote. It offers full media controls, shows state information—like the currently playing app—but also has standard remote functions so you can create a Roku remote card like @iantrich. 

The Roku media player integration is sufficient for lighting automations, though I wish it could detect whether a video is playing or paused. Home Assistant can only detect whether you opened an app on the Roku. The media player status takes 2-3 seconds to update in Home Assistant.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/roku-ha.png" />
        <figcaption>
          <strong>Home Assistant: Great</strong><br>Automatically detected in HA.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Average</strong><br> Works,but no deep integration with apps like Youtube TV
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/roku-app-01.png" />
      <figcaption>
        <strong>Roku App: Great</strong><br>Standard remote control on the Roku app.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/roku-app-02.jpg" />
       <figcaption>
         <strong>Roku App: Great</strong><br>Standard controls, browse videos, and listen to TV audio through phone’s headphone jack.
       </figcaption>
      </figure>
	</div>
</div>


<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\chromecast.jpg" alt=""/>
 <figcaption>
The Chromecast Ultra. <strong>| Google</strong>
 </figcaption>
</figure>

## Chromecast

**Even though I use Chromecast in my home, I find it difficult to recommend as the sole media device in your home because it lacks a TV user interface and remote.** I believe most people want a remote to browse videos, so I recommend trying a Roku, Android TV, or both Roku and Chromecast for these features. My roommates prefer to ignore the Chromecast altogether for the lack of a remote.

I initially liked the Chromecast because it would show video thumbnails on Home Assistant when watching Hulu and Youtube. I thought this feature worked on all apps, but further testing shows the feature doesn’t work on Netflix, Plex, or anything else. Casting from a web browser works, unlike my experiences with Miracast. 

Though Chromecast is supported by a crazy amount of apps, the Google Assistant integration with Chromecast is severely lacking. 

### Installation and Smart Home Integration

Out of all the devices I tested, Chromecast has the best integration with Home Assistant. Status updates are instant, and episode thumbnails show when using Youtube and Hulu--though not for any other app. Home Assistant can also detect pause/play, which the Roku and Amazon Fire TV cannot do. It's not a deal breaker in any way, but I got a kick ~out of it when the lights turned on after pausing the movie.

Voice control on Chromecast is only useful for the deeper integration with Youtube TV, Netflix, HBO, Starz, and Viki, but not available on Hulu, Prime Video, Dramafever, or Vudu.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/other/chromecast-ha.gif" />
        <figcaption>
          <strong>Home Assistant: Great</strong><br>Easy to setup. Instant status, full media control. Thumbnails only work on Hulu and Youtube.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Average</strong><br> Only a few apps support deep voice integration.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/na.png"  />
      <figcaption>
        <strong>SmartThings: N/A</strong><br>Integration does not exist.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/chromecast-tv-app.png" />
       <figcaption>
         <strong>Google Home App: Average</strong><br>Basic controls, no context.
       </figcaption>
      </figure>
	</div>
</div>

<p></p>


<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\amazon-firetv.jpg" alt=""/>
 <figcaption>
   The Amazon Fire TV2. The GOAT! <strong>|  Amazon</strong>
 </figcaption>
</figure>

## Amazon Fire TV

**If you’re using Amazon Echo and Alexa, then the Amazon Fire 4K TV sticks are hard to pass up for its low price, but the lack of Youtube and Youtube TV support makes this a non-contender for me.** I heard about an unofficial Youtube/Youtube TV app called **Smart Youtube TV**, but I can't say if the app will still work a year from now. Voice control is impressive, supporting Hulu and some other network TV apps — why can’t Chromecast support Hulu as well?

### Installation and Smart Home Integration

Fire TVs are moderately difficult to setup in Home Assistant, requiring install of ADB and use of a command-line interface. Home Assistant integration is sufficient for lighting automations, though I wish it could detect whether a video is playing or paused — it only detects whether an app is opened. Player status takes 5 to 10 seconds to update in Home Assistant. I also experienced slight delays when sending pause/play commands from Home Assistant. Keep in mind, I tested a first generation Amazon Fire TV stick, which is the slowest Fire TV device.





