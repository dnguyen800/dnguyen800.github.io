---
layout: page
title: Indoor Cameras
short_title: indoor-camera
excerpt: With a security camera, you are one step closer to being a paranoid old man.
competitors: "Nest, Ring, Wyze, Arlo, Blink, Laview, D-Link, Hikvision, Xiaomi, Simplisafe, Abode, Canary"
update: "<strong>Jan 17, 2021:</strong>First update in two years!  I reviewed the Wyze Cam Pan, which is not worth it!"
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
| **Nest Cam Indoor** | **Wyze Cam v2**<br>**Wyze Cam Pan** | **Xiaomi Xiaofang 1080p Camera** 

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
  <li>Additional verification if a sensor goes off and someone is potentially breaking into your home.</li>
  <li>Place a camera in the garage to confirm the door is closed. Acts as a secondary check of who is coming in/out of the garage.</li>
  <li>Monitor pets or babies.</li>
  <li>If a sensor goes off in the house while you’re away, cameras can provide visual verification of intruders.</li>
</ul>


### Recommended reading

<ul class="alt">
  <li>The Wirecutter's recommendation for <a href="https://thewirecutter.com/reviews/best-wi-fi-home-security-camera/">home security camera</a></li>
  <li>Article from Homealarmreport.com about using <a href="https://homealarmreport.com/using-wyze-cam-with-and-without-a-microsd-card/">Wyze Cam's new features</a></li>
  <li>Mozilla's <b>Privacy Not Included</b> analysis of the <a href="https://foundation.mozilla.org/en/privacynotincluded/products/wyzecam/">WyzeCam</a></li>
  <li><strong>Affiliate Link:</strong> Purchase the <a href="https://amzn.to/2XKbbj8">Nest Indoor Camera</a> and <a href="https://amzn.to/2KFtMZY">Wyze Cam v2</a> from Amazon</li>
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

**If you plan to buy only one camera, then get a quality camera that supports continuous recording, like the [Nest Indoor Camera](https://amzn.to/2XKbbj8).**  Although I talk about Nest often, that doesn’t mean I recommend them to everyone. There are many similar quality cameras that have continuous recording and offer better free storage tiers than Nest, but I chose Nest because I believe their products will be supported for a long time. For other camera recommendations, start by checking out the [Wirecutter’s guide](https://thewirecutter.com/reviews/best-wi-fi-home-security-camera/). I think Nest is a safe choice if you are comfortable using a cloud-connected camera and already in the Google ecosystem because not many security cameras work well with Google to allow live camera feeds on Chromecast or Google smart displays.

The value of Nest cameras is in its ease of setup and use. There are many issues I have using cheaper cameras—wireless range, connection dropouts, unreliable cloud servers—but I haven’t run into any of those issues with Nest. Once you have the camera plugged in and the Nest app installed, everything works reasonably well out of the box. The Nest app is also lightning fast at loading live and recorded footage—it takes under 10 seconds to load the app, authenticate and access my cameras. Whether the improved experience is worth the premium price of Nest products is up to you.

The biggest downside to Nest cameras are that they are cloud-only and do not support local video streaming like RTSP. You wouldn't be able to use the camera on popular apps like Blue Iris, Shinobi, motionEye, Synology Surveillance Station, or Home Assistant. This matters most to advanced DIYers or those concerned about privacy over convenience.

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

Nest’s motion detection algorithm also left me disappointed. I’ve received false alerts from moving window blinds and sunlight piercing through the windows. There are workarounds with camera placement and angle, but I expected the best from a Nest camera.


### Installation and Smart Home Integration

Nest works well with Google Assistant, though there isn’t much need for voice control of a camera, except to broadcast messages or live camera feeds to a Chromecast or a smart display. 

Home Assistant integration is unreliable due to Google shutting down the "Works with Nest" API in 2019, then spinning up a new program called Google Nest Device Access program, which was announced on September 2020. The new program works with Home Assistant as an official integration, though I haven't tested it. With Google's reputation for shutting things down after a few years, I wouldn't expect this program to last much longer than the previous one. There is still hope--for example, Nest cameras will work with Samsung Smartthings starting in January 2021. This recent event is likely due to contracts being signed and wads of cash being shared between the two.

You're better off using the Nest app than trying to do something useful with the livestream in Home Assistant.

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

**The [Wyze Cam v2](https://amzn.to/2KFtMZY), and now, the Wyze Cam v3, continues to add great value for the price and features it offers—I think everyone should have a Wyze as a spare camera.** As a dedicated security camera, there are too many faults with Wyze (and any cheap camera) that I wouldn't trust one to notify me of security incidents. Originally, I had a slightly negative opinion about this camera, but the slew of new features added in 2018 like continuous and extended event recording, local storage, and RTSP support make it hard not to change my mind. If Wyze ever releases a high-quality camera at an affordable price, then I am on board.

Despite using a cheap camera and hardware, Wyze engineers have figured out reasonable workarounds for previous issues like the max 12-second recording time, or the five minute cooldown periods between events. Viewing locally stored footage through your phone's cellular network is possible too! As long as you have a compatible micro SD card (and who doesn’t), the Wyze cam will get these features. [Homealarmreport.com](https://homealarmreport.com/using-wyze-cam-with-and-without-a-microsd-card/) offers a good, detailed breakdown of the features for those interested.

Motion detection in cameras is a balancing act. Should the processing be handled locally or in the cloud? Is there enough processing power to do it locally? Wyze handles motion detection within reason, though it takes some testing and the right camera angle to find the right balance. In one example, I set up a Wyze camera in an empty apartment to monitor for break-ins. I wanted to detect any large changes, like the opening of a door, but I was getting false alerts from sunlight and weather changes. I eventually found the right sensitivity settings for my needs, though it took some trial and error. I still have problems with false positives coming from changes in lighting from the windows, for example.

As of 2021, there are a slew of competitors entering in the low-price camera market: Eufy and Amcrest are making some quality cameras at similar prices. They are itching to get some of that monthly subscription revenue.

### The Problems

I'll be honest--when I initially wrote this review, I only tested the basic functions for a few weeks. That's how reviews are and why you shouldn't trust reviewers who only use the product for a few days. Now that I've used the camera for almost a year, I have plenty of negative experiences to talk about, though I keep my expectations in line with the camera's price. You can't expect an amazing camera for $20, but you can expect a camera that's useful in some scenarios.

In short, Wyze offers many features on paper that sound like it is comparable to a $100 camera, but the user experience highlights the difference between a cheap Wyze cam and an expensive one, like the Nest cameras.

Continuous recording is offered if you install an SD card in the camera, but scrolling through footage in the app is incredibly slow and amounts to a huge waste of time. This is understandable--the continuous footage is stored on the camera's slow SD card. If you're accessing the footage on your phone app over a cellular network, then the camera is limited by your home's internet upload speed and the slow processor in the camera. There are many variables here that result in a usable but sub-par experience.

Without an SD card, the original limitations of the camera are back. Recordings are limited to 10 to 12 seconds, with a five-minute cooldown between each alert. I've read on the Wyze forums that some people are experiencing SD card failures using the continuous recording feature.  The app is a little slower than Nest, and it takes longer to load live footage, but these are reasonable compromises for a $25 camera.

Person detection through the cloud is spotty--I suspect due to the quality of the camera's footage. I receive event notifications late, ranging from 1 to 20 minutes. It's not good to use as a security camera, but is acceptable if you want to see when a delivery person drops off a package.

RTSP support is great on paper, but the execution is poor. This blog [post](https://n1ckyrush.com/en/blog/3-how-to-make-wyzecam-stream-stable-hls-instead-of-rtsp) highlights the problems: gaps in recording, periodic disconnects, green artifacts in videos due to lost packets. I think the developers are running into the limits of the cheap hardware.

There is usually a catch when a company offers a camera and free video recordings at a ridiculously low price.  At the time of this writing, all Wyze wants to do is sell you more stuff. The company is expanding its smart home presence with the introduction of low-priced motion and contact sensors and a DIY NAS video storage solution.  That is a reasonable strategy that I'm okay with.

The Mozilla Foundation, interestingly enough, wrote a [privacy-focused analysis](https://foundation.mozilla.org/en/privacynotincluded/products/wyzecam/) on the Wyze camera and rates it as “Meets our minimum security standards.”

I generally do not recommend using any Wyze camera custom firmware as you lose existing functionality. I’ve tried hacks on similar cameras (Xiaofang) and found that the loss of features like automatic night vision, cloud, or reliable motion detection wasn’t worth the trade-off.

### Installation and Smart Home Integration

Viewing camera footage in Home Assistant and SmartThings is not a good experience in general—for that reason, the Wyze app is better for reviewing alerts and accessing camera footage.  The recent Wyze beta firmware allows for Real Time Streaming Protocol (RTSP), which allows for platforms like Home Assistant to use the camera with the [**``Generic IP Camera``**](https://www.home-assistant.io/components/generic/) component.

Google Assistant integration is coming to Wyze, but it's currently in beta. I suppose it would be useful to stream camera footage onto a Chromecast device, like the Lenovo 10" Display I use in my room.

<!-- Product Review section -->
<hr class="major" />
<figure class="align-left">
 <img src="assets\images\product-photo\wyze-cam-pan.jpg" alt=""/>
 <figcaption>
<b>|  Wyze</b>
 </figcaption>
</figure>

## Wyze Cam Pan

**The Wyze Cam Pan is essentially the same as the v2, including all of its faults, except with panning controls.** Here is my short review.

The panning controls technically work, but only through the Wyze app. The camera is not ONVIF-compatible so panning controls are not usable in any other app or Home Assistant.

The automated tracking feature is garbage. The camera will contstantly spin left and right, failing to focus on the object in motion. In the end, you get some blurry camera footage. I tested this by watching a puppy in his play area, which the camera's field of view already covered the area, but it would still pan left and right constantly.

The camera feels really tall. There are newer cameras from Amcrest and Eufy that are 1" shorter and (hopefully) better.

I paid an extra $10 for manual panning controls. Not worth it.