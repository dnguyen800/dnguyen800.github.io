---
layout: page
title: Indoor Cameras
short_title: indoor-camera
excerpt: With a security camera, you are one step closer to being a paranoid old man.
competitors: "Nest, Ring, Wyze, Arlo, Blink, Laview, D-Link, Hikvision, Xiaomi, Simplisafe, Abode, Canary"
permalink: /indoor-camera
image: assets/images/overlay-ws/indoor-camera.jpg
image_credit: Warner Bros.
categories: 
    - "Camera"
    - "Security"
    - "Home Automation"

---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\nest.png){:.image.logo} |  ![](assets\images\logo\wyze.png){:.image.logo} | ![](assets\images\logo\xiaomi.png){:.image.logo}
|:-:|:-:|:-:
| **Nest Cam Indoor** | **Wyze Cam v2** | **Xiaomi Xiaofang 1080p Camera** 

## What you need to know

For privacy reasons, I am very cautious when it comes to the placement of indoor cameras. In my household, we have a camera in the living room that covers all the entry points into the house while avoiding areas where I and my roommates frequent. With the help of presence sensors, I can turn off the camera when someone is at home. My goal is to provide additional security in my home, not invade the privacy of my household members.

Besides using as a pet or baby monitor, cameras can provide visual confirmation of intruders. I wouldn’t make a 911 call based on sensors alone unless the alarm system wasn’t disabled timely. What if I forgot that a relative was stopping by? 

Even if it was only me being recorded on my camera, it doesn’t feel right to be recorded. Maybe that is because there is the possibility of someone other than me viewing the camera footage. Whether it is a rogue IT admin at the company, someone with access to the servers storing the footage, or a hacker who obtained user credentials or exploited a vulnerability on the camera—it is possible that someone can view your footage without permission.

There is a good selection of cameras at different price ranges. My recommendation is to buy one quality camera and one cheap camera to cover your bases. Though if you’re rich, feel free to go nuts with the cameras and the spying.

### Considerations before buying an indoor camera

<ul class="alt">
  <li><b>Check with household members about installing any indoor cameras.</b> Privacy should be respected, after all.</li>
  <li><b>Decide whether you want local or cloud storage features.</b></li>
  <li><b>Cameras can be powered by battery, AC or ethernet cable (using Power-over-ethernet, or PoE).</b></li>
  <li>See what is offered in the camera company's free video storage tier.</li>
  <li>Look into how app notifications are handled if the camera works locally only. Can you get motion detection alerts on your phone if you're not on the same Wi-Fi network?</li>
  <li><b>Do a quick search on the company's history with security vulnerabilities.</b> You will be surprised at how many well-known companies have gaping security flaws.</li>
</ul>

### What you get with an indoor camera

<ul class="alt">
  <li>Place a camera in the garage to confirm the door is closed. Acts as a secondary check of who is coming in/out of the garage.</li>
  <li>Monitor pets or babies.</li>
  <li>If a sensor goes off in the house while you’re away, cameras can provide visual verification of intruders.</li>
</ul>


### Recommended reading

<ul class="alt">
  <li>The Wirecutter's recommendation for <a href="https://thewirecutter.com/reviews/best-wi-fi-home-security-camera/">home security camera</a></li>
  <li>Article from Homealarmreport.com about using <a href="https://homealarmreport.com/using-wyze-cam-with-and-without-a-microsd-card/">Wyze Cam's new features</a></li>
  <li>Mozilla's <b>Privacy Not Included</b> analysis of the <a href="https://foundation.mozilla.org/en/privacynotincluded/products/wyzecam/">WyzeCam</a></li>
  <li><strong>Affiliate Link:</strong> Purchase the <a href="https://amzn.to/2Vwui2h">Nest Indoor Camera</a> and <a href="https://amzn.to/2INEX2x">Wyze Cam v2</a> from Amazon</li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
 <img src="assets\images\product-photo\nest-indoor.jpg" alt=""/>
 <figcaption>
The Nest Indoor Camera. <strong>|  Google</strong>
 </figcaption>
</figure>

## Nest Cam Indoor

**If you plan to buy only one camera, then get a quality camera that supports continuous recording, like the [Nest Indoor Camera](https://amzn.to/2Vwui2h).**  Although I talk about Nest often, that doesn’t mean I recommend them to everyone. There are many similar quality cameras that have continuous recording and offer better free storage tiers than Nest, but I chose Nest because I believe their products will be supported for a long time. For other camera recommendations, start by checking out the [Wirecutter’s guide](https://thewirecutter.com/reviews/best-wi-fi-home-security-camera/).. I think Nest is a safe choice if you are comfortable using a cloud-connected camera and already in the Google ecosystem because not many security cameras work well with Google to allow live camera feeds on Chromecast or Google smart displays.

The value of Nest cameras is in its ease of setup and use. There are many issues I have using cheaper cameras—wireless range, connection dropouts, unreliable cloud servers—but I haven’t run into any of those issues with Nest. Once you have the camera plugged in and the Nest app installed, everything works reasonably well out of the box. The Nest app is also lightning fast at loading live and recorded footage—it takes under 10 seconds to load the app, authenticate and access my cameras. Whether the improved experience is worth the premium price of Nest products is up to you.

<figure class="align-center">
 <a class="image-link" href="assets\images\other\nest_aware.png" ><img src="assets\images\other\nest_aware.png" alt="" /></a>
 <figcaption>
The new pricing for Nest Aware monthly plans.
 </figcaption>
</figure>

The **Nest Aware** monthly service used to be the most expensive of the competition, but at the time of this writing,  Nest introduced a $5/month pricing tier. This is much more affordable and I don’t feel as bad anymore when recommending Nest products to customers. Though if you plan on getting a Ring security system, any Ring camera monthly fees are included with their security monitoring fee, making Ring the most affordable and comprehensive security option. 

Nest sends notifications when the camera is offline (due to a power outage, or someone unplugging the cord). It’s a nice feature that other companies have.

### The Problems

There is a **Home/away Assist** feature on the Nest app, but I found it doesn’t work reliably. There were a few times when I received an alert and opened the Nest app to see my roommate in the living room, watching TV (luckily G-rated shows). I’ve done my own testing of the feature (Home Assistant integration gives you access to this data) and found it can take hours for Nest to update to Home or Away status. As phones get more aggressive with battery saving, a lot of apps are going to have trouble with presence detection. Unfortunately, Nest has not solved this issue either.

Nest’s motion detection algorithm also left me disappointed. I’ve received false alerts from moving window blinds and sunlight piercing through the windows. There are workarounds with camera placement and angle, but I expected more from a Nest camera.

### Installation and Smart Home Integration

Nest works well with Google Assistant, though there isn’t much need for voice control of a camera, except to broadcast messages or live camera feeds to a Chromecast or a smart display. 

Home Assistant integration works with a Nest developer account, though the Nest camera feed in Home Assistant is only a still image that’s updated every few seconds. It’s better to use the Nest app for viewing live and recorded footage. Nest detection alerts can be tracked in Home Assistant, so you can pair an automation with it, like, blinking the lights when someone is at the door. I never found the need to use it though. 


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/nest-indoor-ha.png" />
        <figcaption>
           <b>Home Assistant: Okay</b><br>It works, but impossible to see real-time footage. The ‘motion detected’ sensor can be used for automations.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
          <b>Voice: Great</b><br>Can send broadcast messages when someone is at the door.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/nest-indoor-st.png" />
      <figcaption>
         <b>SmartThings: Okay</b><br> NST Manager SmartApp shows camera feed, but it's not real-time.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/nest-indoor-app.jpg"  />
       <figcaption>
         <b>Nest App: Great</b><br>Simple, easy-to-use.
       </figcaption>
      </figure>
	</div>
</div>

<p></p>


<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
 <img src="assets\images\product-photo\wyze.jpg" alt=""/>
 <figcaption>
<b>|  Wyze</b>
 </figcaption>
</figure>

## Wyze Cam v2

**The [Wyze Cam v2](https://amzn.to/2INEX2x) continues to add great value for the price and features it offers—I think everyone should have one as a cheap, spare camera.** Originally, I had a slightly negative opinion about this camera, but the slew of new features added in 2018 like continuous and extended event recording, local storage, and RTSP make it hard not to change my mind. If Wyze ever releases a high-quality camera at an affordable price, then I am on board.

Despite using a cheap camera and hardware, Wyze engineers have figured out reasonable workarounds for previous issues like the max 12-second recording time, or the five minute cooldown periods between events. Viewing locally stored footage through your phone's cellular network is possible too! As long as you have a compatible micro SD card (and who doesn’t), the Wyze cam will get these features. [Homealarmreport.com](https://homealarmreport.com/using-wyze-cam-with-and-without-a-microsd-card/) offers a good, detailed breakdown of the features for those interested.

Motion detection works reasonably well, though it takes some testing to find the right settings. In one example, I set up a Wyze camera in an empty apartment to monitor for break-ins. I wanted to detect any large changes, like the opening of a door, but I was getting false alerts from sunlight and weather changes. I eventually found the right sensitivity settings for my needs, though it took some trial and error.

### The Problems

Without an SD card, the original limitations of the camera are back. Recordings are limited to 10 to 12 seconds, with a five-minute cooldown between each alert. I've read on the Wyze forums that some people are experiencing SD card failures using the continuous recording feature.  The app is a little slower than Nest, and it takes longer to load live footage, but these are reasonable compromises for a $25 camera.

There is usually a catch when a company offers a camera and free video recordings at a ridiculously low price.  At the time of this writing, all Wyze wants to do is sell you more stuff. The company is expanding its smart home presence with the introduction of low-priced motion and contact sensors and a DIY NAS video storage solution.  That is a reasonable strategy that I'm okay with.

The Mozilla Foundation, interestingly enough, wrote a [privacy-focused analysis](https://foundation.mozilla.org/en/privacynotincluded/products/wyzecam/) on the Wyze camera and rates it as “Meets our minimum security standards.”

I generally do not recommend using any Wyze camera custom firmware as you lose existing functionality. I’ve tried hacks on similar cameras (Xiaofang) and found that the loss of features like automatic night vision, cloud, or reliable motion detection wasn’t worth the trade-off.

### Installation and Smart Home Integration

Viewing camera footage in Home Assistant and SmartThings is not a good experience in general—for that reason, the Wyze app is better for reviewing alerts and accessing camera footage.  The recent Wyze beta firmware allows for Real Time Streaming Protocol (RTSP), which allows for platforms like Home Assistant to use the camera with the [**``Generic IP Camera``**](https://www.home-assistant.io/components/generic/) component.

Google Assistant integration is coming to Wyze, but it's currently in beta. I suppose it would be useful to stream camera footage onto a Chromecast device, like the Lenovo 10" Display I use in my room.