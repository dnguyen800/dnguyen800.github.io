---
layout: page
title: Smart Bulbs
short_title: smart-bulb
excerpt: For the renters out there, smart bulbs are a useful (and the only) smart lighting option. 
competitors: "Philips Hue, Ikea Tradfri, Xiaomi, Sengled, Sylvania, TP-Link, Lifx, Eufy"
permalink: /smart-bulb
image: assets/images/overlay-ws/smart-bulb.jpg
image_credit: Dan Nguyen
categories: 
    - "Lighting"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\philips-hue.png){:.image.logo} |  ![](assets\images\logo\sengled.png){:.image.logo} | ![](assets\images\logo\tplink.png){:.image.logo} | ![](assets\images\logo\osram.png){:.image.logo}
|:-:|:-:|:-:|:-:
| **White A19 60W** | **Element Classic A19 White**<br>**Element Classic BR30 White** | **Wifi Color (LB230)** | **Full Color (A19C)**<br>**Full Color (BR30C)**


## What you need to know

For me, smart bulbs were the only way I could start experimenting with smart homes. I was renting at the time and couldn’t make any house modifications, so I bought a smart bulb, a Wi-Fi outlet, and a Google Home speaker to satisfy that itch. What I didn’t realize was that I couldn’t use the light switch and smart bulb at the same time, since the switch cuts off power to the bulb. It was awkward telling my roommates they could no longer use the light switch, but once my lighting automations became reliable, there was no need to use the switch anymore. 

I’m still a renter, so I use smart bulbs around the house. Smart bulbs remain a cheaper, portable lighting solution compared to smart switches. I can mitigate most of the issues with smart bulbs and live with the rest. 

<p class="box">
<strong>Smart Bulbs Acting As Zigbee Repeaters</strong><br>
<i>I have not personally verified this information but some smart bulbs can act as Zigbee network repeaters, though it varies by brand. Philips Hue bulbs repeat for Hue bulbs only. Sengled bulbs are not repeaters, but the rest are, I think. It goes without saying that if the smart bulb’s power is shut off by a light switch, it no longer functions as a repeater.</i></p>

### Considerations before buying a smart bulb

<ul class="alt">
  <li><strong>Smart bulbs won’t respond if its power is cut off by the light switch.</strong></li>
  <li><strong>Most smart bulbs on sale are Zigbee or Wi-Fi.</strong> I’ve never seen an affordable Z-Wave bulb before.</li>
</ul>

### What you get with a smart bulb

<ul class="alt">
  <li>Light bulbs that can be controlled by automations.</li>
  <li>Colored lighting. I haven’t found a good use case for it unless you’re throwing colorful raves.</li>
  <li>Some smart bulbs can act as Zigbee network repeaters, though not many other devices besides light bulbs use Zigbee.</li>
</ul>


### Recommended Reading

<ul class="alt">
  <li>Slickdeals sales on <a href="https://slickdeals.net/newsearch.php?forumchoice%5B%5D=4&forumchoice%5B%5D=9&forumchoice%5B%5D=10&forumchoice%5B%5D=13&forumchoice%5B%5D=25&forumchoice%5B%5D=30&forumchoice%5B%5D=38&forumchoice%5B%5D=39&forumchoice%5B%5D=41&forumchoice%5B%5D=44&forumchoice%5B%5D=53&forumchoice%5B%5D=54&forumchoice%5B%5D=71&q=philips+hue&firstonly=1">Philips Hue bulbs</a></li>
  <li>Convert a Philip Hue light bulb (or any Zigbee bulb) to a standard Zigbee bulb using the <a href="https://github.com/mozilla-iot/wiki/wiki/HOWTO:-Factory-reset-a-Hue-bulb">Philips Hue dimmer remote</a> or the <a href="https://community.home-assistant.io/t/hue-thief-and-hass-io/48420/10">Hue Thief script</a>.</li>
  <li><strong>Affiliate Link:</strong> Purchase the <a href="https://amzn.to/31tq9fr">Philips Hue Starter Kit</a>, <a href="https://amzn.to/2IJoA4O">TP-Link Kasa Wi-Fi bulb</a>, <a href="https://amzn.to/2ICIwWJ">Sylvania Osram Lightify bulbs</a> or <a href="https://amzn.to/2MUyHcm">Sengled Element Classic bulbs</a> on Amazon</li>
</ul>


<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
  <img src="assets\images\product-photo\philips-hue.png" alt=""/>
  <figcaption>
    The Philips Hue collection. <strong>|  Philips</strong>
  </figcaption>
</figure>

## Philips Hue

**If you don’t mind using adding yet another hub to the network and paying a slight premium, then the [Philips Hue](https://amzn.to/31tq9fr) series of light bulbs offers consistently high-quality smart bulbs that are always available on the market.** Those on a budget don’t need to go with Philips Hue, but it’ll take more research to get a high-quality bulb like Philips Hue.  I’ve tried other smart bulbs that range from average to just as good as Philips Hue, but those I would recommend are no longer available on the market. I recommend Philips Hue because I know they are good and available on Amazon.

The Philips Hue bulbs pair well with the Hue light strips that make up my media center lighting. Watching the living room lights fade out as the TV light strips brightens is a very cool transition that easily impresses folks. If you’re not particular about the fade effect or color accuracy, then any cheap Zigbee bulb under $10 should work for you.

<figure class="align-center">
  <div class="container">
   {%- include extensions/youtube.html id='39FGJ40vfHs' -%}
  </div>
  <figcaption>Example of the Philips Hue fade effect.</figcaption> 
</figure>
<p></p>

### The Problems
Philips Hue bulbs require the Hue bridge because it uses a different profile of Zigbee—called ZLL—that is not compatible with the Zigbee ZHA bulbs on the market. So you can’t normally pair Hue bulbs to SmartThings (though not impossible, see next section). You also don’t get the benefits of repeaters in your Zigbee network if you’re mixing and matching Hue bulbs with other Zigbee bulbs. Hue bulbs act as repeaters for Hue lights only and most Zigbee bulbs act as repeaters except for a few brands like Sengled.

### Using Hue bulbs without the Hue Bridge

It’s possible to flash Hue bulbs to standard Zigbee ZHA bulbs using a Python script called [**``Hue Thief``**](https://community.home-assistant.io/t/hue-thief-and-hass-io/48420/10), but I don’t recommend it because of the difficulty in getting it to work and factory resetting bulbs. To begin the process, you need to purchase a Zigbee USB radio, like the [**``GoControl HUSBZB-1``**](https://amzn.to/2DH8G95), which is redundant if you already have a SmartThings or Hubitat device. Following my tutorial may not work for everyone, as indicated on the forum.

I’ve had issues with flashed Hue lights unpairing from my network and I haven’t found a solution yet, because there isn’t a normal way for the Hue light to enter exclusion mode! I hear it’s possible to factory reset Philips Hue bulbs using a [**Philips dimmer remote**](https://amzn.to/2DDMZac), as described [here](https://github.com/mozilla-iot/wiki/wiki/HOWTO:-Factory-reset-a-Hue-bulb). This seems like a better alternative but I didn’t want to spend another $25 to find out.

### Installation and Smart Home Integration

Compatibility is not an issue as Philips Hue supports nearly every home automation hub out there. SmartThings, Home Assistant, Hubitat, Alexa, Google Assistant—they are all officially supported. Another plus is that the hub is controllable on the local network so Home Assistant can control the Hue lights without an internet connection. That is either very forward thinking or lazy of Philips to provide that option. 

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/philips-hue-ha-01.png" />
        <figcaption>
          <strong>Home Assistant: Great</strong><br> Press a button on the Hue hub to pair with HA. Super easy. 
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Great</strong><br>Connect Hue to either SmartThings, Google Home or Alexa for voice control.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/philips-lightstrip-st.png" />
      <figcaption>
      <strong>SmartThings: Great</strong><br> A Philips Hue light strip looks like this in ST.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/philips-hue-app.png"  />
       <figcaption>
         <strong>Phlips Hue App: Good</strong><br>Basic lighting and scenes functions. 
       </figcaption>
      </figure>
	</div>
</div>
<p></p>


<!-- Product Review section -->
<hr class="minor" />

## The Competition

<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\kasa.jpg" alt=""/>
        <figcaption> Kasa bulbs <strong>| TP-Link</strong></figcaption>
      </figure>
      <h3>TP-Link LB230 Kasa Wifi </h3>
      <p><strong>While the <a href="https://amzn.to/2IJoA4O">TP-Link Kasa LB230 Wifi bulbs</a> are quite good -- they respond quickly and are compatible with Home Assistant and Google Assistant -- I still don’t recommend buying Wi-Fi bulbs due to potential compatibility and security issues.</strong>  SmartThings integration using a custom device handler is dependent on an internet connection to TP-Link servers, which can go offline in the future. The Kasa app is also insecure according to this <a href="https://www.tomsguide.com/us/smart-home-leaky-apps,news-29319.html">study</a>, so I would expect the bulb (which is on your personal network) has potential vulnerabilities too. If TP-Link were to go offline, only Home Assistant would be able to use the bulbs via local communication.  </p>
    </div>
    <div class="6u$ 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\osram.jpg" alt=""/>
        <figcaption>
         Lightify bulbs <strong>| Osram</strong>
        </figcaption>
        </figure>
    	<h3>Osram Sylvania Lightify</h3>
    	<p><strong>The <a href="https://amzn.to/2ICIwWJ">Sylvania Osram Lightify Bulbs</a> are the perfect smart bulbs for your home automation hub -- I would buy more of these if they were still available.</strong> They are Zigbee bulbs and pair with SmartThings easily, responds instantly and has a fade effect like Hue bulbs. During the last sale found on Slickdeals, the colored bulbs could be found for $10-15, which is the lowest price for colored bulbs I have ever seen. The only reason I would not buy this is if the Zigbee network is unreliable in your home.</p>
    </div>

    <div class="6u$ 12u$(small)">
        <figure class="align-left">
          <img src="assets\images\product-photo\sengled.jpg" alt=""/>
        <figcaption>
         Element Classic <strong>| Sengled</strong>
        </figcaption>
        </figure>
    	<h3>Sengled Element Classic</h3>
    	<p><strong>At $7 each, the <a href="https://amzn.to/2MUyHcm">Sengled Element Classic bulbs</a> (BR30 and A19 sizes) are the cheapest functioning Zigbee bulbs I could find, though it lacks nice-to-have features like the fade effect.</strong> Though that is not a big deal if you plan on sticking these lights in the garage or some unnoticeable place.  These bulbs are Zigbee and I haven't had any problems with pairing or disconnections, so at least they are reliable. I miss the Hue fade effect though, and would gladly pay a few more dollars for a nicer bulb than the Sengled Element. </p>
    </div>

</div>



