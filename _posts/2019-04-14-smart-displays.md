---
layout: page
title: Smart Displays
short_title: smart-display
excerpt: It's like a  tablet, but less useful.
competitors: "Lenovo, JBL, Google, Amazon, Facebook"
permalink: /smart-display
image: assets/images/overlay-ws/smart-display.jpg
image_credit: Dan Nguyen
categories: 
    - "Gadgets"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\lenovo.png){:.image.logo} 
|:-:
| **Lenovo Smart Display with Google Assistant (10")** 


## What you need to know

Smart displays are a relatively new market in 2018, and I have yet to find what they do best. It is definitely NOT a tablet, as it doesn’t have a web browser or any applications designed for it.  If you think of it as a voice assistant that can visually display search results and as a Chromecast combined, then you can start to appreciate it what it does well. However, it is not an essential item to any smart home yet.

For the right price, I would still prefer a smart display than a dedicated tablet, mainly because of the better overall voice assistant experience. I have tried using Alexa Hands-free on Fire HD tablets, and the experience is not good. Either the tablet is too slow to respond, or it failed to recognize my voice with its single microphone. Smart displays were designed to function as voice assistants from the get-go.

### Considerations before buying a smart display

<ul class="alt">
  <li><strong>A smart display is not a tablet and never will be.</strong> It lacks a web browser and dedicated apps. It's a voice assistant first, display second.</li>
  <li><strong>The Home Assistant, SmartThings apps aren’t available on the Google displays</strong>, though you can access some of the same devices connected to Google Home.</li>
</ul>


### What you get with a smart display

<ul class="alt">
  <li>A dedicated voice assistant and a visual display for a photo frame, clock, weather.</li>
  <li> A Chromecast device to cast videos and music.</li>
  <li>A digital photo frame that connects to Google Photos.</li>
  <li>Basic control of lighting—anything controllable with Google Assistant works here.</li>
  <li>A basic kitchen assistant/recipe display from the more popular food recipe sites.</li>
</ul>

### Recommended reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2YTSQ3R">Lenovo 10" Display</a> on Amazon</li>
  <li><a href="https://arstechnica.com/gadgets/2019/02/android-things-is-no-longer-for-things-focuses-on-smart-speakers-and-displays/">Article</a> about Google pivoting the Android IoT platform.</li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
  <img src="assets\images\product-photo\lenovo-smart-display.jpg" alt=""/>
  <figcaption>
    The Lenovo 10" display. <strong> |  Lenovo</strong>
  </figcaption>
</figure>

## Lenovo Smart Display 10” with Google Assistant

**The Lenovo Smart Display was the first Google Assistant-powered smart display to be released, but with Google's recent pivot of Android Things platform, the future of the display looks grim.** Despite having some useful features like **``Chromecast Built-in``**, a quality display, speaker and microphones, web app support is limited and unlikely to come in the future. No developer is going to work on a platform for smart displays only when there are other platforms supporting a wider variety of devices.

There have been some fire sales going on for this 10” display—selling for as low as $75, which is an excellent deal for a very nice digital photo frame and decent speakers. As long as you expect the Lenovo display to be a voice assistant and not much more, then the price is a steal for a fully functional Chromecast and Google Home speaker.  

Even if the display doesn't get any new features in the future, I do like the existing features. Setting it up as a photo frame to display any Google Photo album is a great way to show off the beautiful 10" display. I regularly watch Youtube TV and Hulu on the display in my room as I work on this website. The microphone and speakers are of similar quality to the Google Home, which are not hi-fi at all but meet somewhere in the "good enough" category. There are times where I'm impressed the microphone heard what I said, but there are other days where I have to yell into the display.

### The Problems

So when the display was first released in August 2018, Netflix and several other Chromecast functions didn't work. Then a few months later, Netflix was supported. But now (as of April 2019), they removed support again. Netflix is notoriously picky/political about supporting casting modes -- they recently removed Apple Airplay support as Apple is encroaching on their territory with Apple TV+. It's a shame as every other Chromecast-supported app works, and it makes me question the value of my pricey Netflix subscription.

60 frames-per-second content from Youtube is playable, but there is a stutter every few seconds. It's noticeable when watching sports games or videogame playthroughs, but is fine with everything else.

I initially had Wi-Fi connection issues where I would have to run the Google Home setup process again, but I learned the root cause of the issue was with the refurbished TP-Link Onhub router I used. Once I replaced it with a Google Wifi point, I no longer had any trouble streaming videos or maintaining a consistent connection on the display.

<figure class="align-center" style="max-width:442px;" >
 <img src="assets\images\other\lenovo-smart-display-app.png" alt="" />
 <figcaption>
Searching for recipes through Google will pop up the 'Send to Display' button.
 </figcaption>
</figure>

I bought this display with the intention to use as a cooking assistant--mainly for setting timers, doing unit conversions, and reading recipes out loud, but it wasn't very good at the latter. Imagine saying **``Okay Google, next step``** for each recipe step--it gets tiring, fast. Recipes from less popular blog sites aren't available to cast to the display, and I have no other way to load my private collection of recipes. As a kitchen assistant, it could definitely be improved, but it's unlikely we will see any more improvements from Google or Lenovo.


### Installation and Smart Home Integration
The display is a fully functional Chromecast and is automatically detected in Home Assistant as such. Chromecast is the best media player integration I’ve tested so far, and that includes this display. It works with all Chromecast video and audio apps and supports Chromecast multi-room audio. I tested major video apps, but not all of them, so I can't promise every Chromecast app works on the display. When the Lenovo was originally released, multi-room audio and Netflix were not supported (but is now, after an update). I don't know the reason why, but it goes to show you that there are some smaller differences within Chromecast support.

For controlling lights, the display cannot access the Home Assistant UI, but can indirectly control the lights through Google Assistant, which will bring up the screen below:

<figure class="align-center">
 <img src="assets\images\other\smart_display-lenovo-photo01.jpg" />
 <figcaption>
An example of light control with the display. You first must use your voice to control the light for this menu to appear.<strong> | Lenovo</strong> 
</figcaption>
</figure>
<p></p>

You need to connect your Home Assistant instance to Google Assistant, either using Home Assistant Cloud or setting up the component yourself. I rarely use this function as it’s not as effective as using my voice to turn on lights and other devices.