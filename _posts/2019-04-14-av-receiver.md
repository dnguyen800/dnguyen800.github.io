---
layout: page
title: AV Receivers
short_title: av-receiver
excerpt: 'Honest question: who uses more than 25% of the max volume on receivers? If you answered "yes," your neighbors must hate you.'
permalink: /av-receiver
competitors: "Onkyo, Pioneer, Sony, Denon, Yamaha, Marantz"
image: assets/images/overlay-ws/av-receiver.jpg
image_credit: Denon.jp
image_url: https://www.denon.jp/jp/
categories: 
    - "Media"
    - "Home Theater"
    - "Home Automation"

---

<!--more-->
#### I’ve personally tested the following:

|---
| ![](assets\images\logo\pioneer.png){:.image.logo} |  ![](assets\images\logo\onkyo.png){:.image.logo} 
|:-:|:-:
| **VSX-1131 (2016)** | **Onkyo TX-NR509 (2011)** 

## What you need to know

These days, most people don’t own AV receivers and the massive speakers that accompany them. They are bulky and tend to dominate the living room space, so I usually recommend customers invest in a good sound bar for home theater quality sound. If you still want or already have a receiver, then you might as well integrate it with the rest of the smart home. Luckily, the latest AV receivers are easy to integrate into Home Assistant!

There aren’t many AV receiver brands out there, which is good because it’s easier to add support to Home Assistant for the few remaining receivers out there. There is a compatibility list for some integrations, like Denon, but the only way to find out if a specific model works is to try it yourself. 

<p class="box">
<i>If the AV receiver doesn’t have network capabilities, then a universal remote like the Logitech Harmony can achieve some integration but lacks features like state awareness (i.e. knowing if a device is on or off).</i></p>

Voice control is possible if you set up the Home Assistant Cloud with Google Assistant or Alexa, but that shouldn’t be necessary as powering on and changing AV receiver inputs should be handled automatically through **``HDMI-CEC``** and **``ARC``**.

A friend recently asked for AV receiver recommendations, which made me realize how easy it is to buy the wrong AV receiver and cables. From my experience, there are several considerations before buying an AV receiver and HDMI cables:

### Considerations before buying an AV receiver

<ul class="alt">
  <li><b>The receiver should have at least FOUR HDCP 2.2 ports,</b> which is necessary for 4K video. Not all HDMI ports on the receiver are HDCP 2.2. compatible, even the expensive receivers.</li>
  <li><b>The receiver and TV should support HDMI ARC (Audio Return Channel) or eARC</b>, which allows the TV to send audio to the soundbar or AV receiver with a single HDMI cable. This is important if you want surround sound support when using the TV’s smart apps. </li>
  <li><b>The receiver and TV should support HDMI-CEC</b>, also known as Samsung Anynet+, LG  SimpLink, and Sony Bravia Sync. CEC lets devices control the TV and AV receiver inputs automatically. It also allows the TV to automatically turn on the AV receiver.</li>
  <li><b>HDMI cables must be rated at 18gbps to support 4K resolution at 60 frames-per-second.</b> 10gbps is not 4K. In-wall cables should be rated as CL2 to CL3. It’s a safety thing.</li>
  <li> Check the Home Assistant <a href="https://www.home-assistant.io/components">Component page</a> to see if your brand AVR is supported.</li>
</ul>


### What you get with a network-enabled AV receiver

<ul class="alt">
  <li>Get rid of remotes since HDMI ARC, CEC can turn on the TV and change inputs for you.</li>
  <li>Universal remote control of the media center in Home Assistant.</li>
  <li>More specific automations (if Chromecast Audio is playing, then turn on the receiver).</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li>Digital Trends article about <a href="https://www.digitaltrends.com/home-theater/hdmi-arc-explained-works-care/">HDMI CEC, ARC, and eARC</a></li>
  <li>Home Assistant Components for <a href="https://www.home-assistant.io/components/onkyo/">Onkyo</a> and <a href="https://www.home-assistant.io/components/pioneer/">Pioneer</a></li>
  <li>Find AV receivers on sale at <a href="https://slickdeals.net/newsearch.php?forumchoice%5B%5D=4&forumchoice%5B%5D=9&forumchoice%5B%5D=10&forumchoice%5B%5D=13&forumchoice%5B%5D=25&forumchoice%5B%5D=30&forumchoice%5B%5D=38&forumchoice%5B%5D=39&forumchoice%5B%5D=41&forumchoice%5B%5D=44&forumchoice%5B%5D=53&forumchoice%5B%5D=54&forumchoice%5B%5D=71&q=av+receiver&firstonly=1">Slickdeals</a></li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
  <img src="assets\images\product-photo\onkyo.png" alt=""/>
  <figcaption>
    An Onkyo receiver. <b>|  Onkyo</b>
  </figcaption>
</figure>

## Onkyo Receivers

My 2011 Onkyo TX-NR509 receiver is an ancient relic, but surprisingly, it is fully compatible with Home Assistant. Thanks to those folks who reverse-engineered Onkyo’s API and the lack of updates from Onkyo, the receiver correctly reports the power and input state instantly in Home Assistant, and I can remotely turn on change inputs within the UI. Installation is a breeze—type the receiver’s IP address into the Home Assistant configuration and you’re basically done.

### Installation and Smart Home Integration
In the AV receiver settings, be sure to turn off any power saving mode, and enable network standby option. This is necessary for Home Assistant to remotely turn on the receiver.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/onkyo-ha.png" />
        <figcaption>
          <b>Home Assistant: Great</b><br>Easy to set up. Instant status, full media control. 
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <b>Voice: Average</b><br> Works through Onkyo>>HA>>Google Assistant. Basic commands work but not necessary with HDMI-CEC.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/na.png" />
      <figcaption>
      <b>SmartThings: None</b><br> Integration does not exist.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/onkyo-app.png"  />
       <figcaption>
         <b>Onkyo App: Average</b><br>Basic controls. Hasn't been updated in years. Some network functionality (Spotify/Onkyo integration) no longer works.
       </figcaption>
      </figure>
	</div>
</div>

<!-- Competition section -->
<hr class="minor" />

<figure class="align-left">
  <img src="assets\images\product-photo\pioneer.png" alt=""/>
  <figcaption>
    A Pioneer receiver. <b>|  Pioneer</b>
  </figcaption>
</figure>
<p></p>

## Pioneer Receivers

As of 2014, Pioneer and Onkyo are effectively the same company! I tested the 2016 Pioneer VSX-1131 receiver and found out that it uses the [**``Onkyo Component``**](https://www.home-assistant.io/components/media_player.onkyo/) in Home Assistant, and thus provides full media control and responds instantly, just like my Onkyo receiver. Another plus is that this receiver can be powered on over Wi-Fi, which is not always true for every receiver. 

### Installation and Smart Home Integration

In the AV receiver settings, be sure to turn off any power saving mode, and enable network standby option. This is necessary for Home Assistant to remotely turn on the receiver.

Pioneer's installation and smart home integration are exactly the same as the Onkyo integration, so please read that [section](#onkyo-receivers) for details.
