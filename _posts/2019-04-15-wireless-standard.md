---
layout: page
title: Wireless Standard
short_title: wireless-standard
excerpt: Yes, you will need to learn about the available wireless standards for smart homes to avoid buying the wrong sensors and lights.
competitors: "Z-Wave Plus, Zigbee, Wi-Fi, Bluetooth LE, Homekit, Thread"
permalink: /wireless-standard
image: assets/images/overlay-ws/wireless-standard.jpg
update: "<strong>April 15, 2019:</strong> Added my experience with Zigbee network interference."
image_credit: Dan Nguyen
image_url: about
categories: 
    - "Infrastructure"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

| ![Z-Wave](assets\images\logo\zwave.png){:.image.logo} | ![Zigbee](assets\images\logo\zigbee.png){:.image.logo} | ![Wi-Fi Based](assets\images\logo\wifi.png){:.image.logo} | ![Homekit](assets\images\logo\homekit.png){:.image.logo} |
|:-------:|:--------:|:---------:|:---------:|
| **Z-Wave Plus** | **Zigbee** | **Wi-Fi (Wemo, Kasa)** | **HomeKit** |


## What you need to know
There is yet another set of wireless standards in the smart home space that you need to be familiar with. Popular standards like Wi-Fi, Bluetooth, RF and infrared didn’t quite make the cut for smart home use, so we’re left with two newish standards: Zigbee and Z-Wave. Each has their set of advantages and disadvantages with no clear winner.

Your hub supports most of the wireless standards (Zigbee, Z-Wave, Wi-Fi), but connected devices usually support only one of those standards. Adding to the confusion are companies like Philips, Ikea, Sengled, and Xiaomi selling their own Zigbee hubs that are compatible with their respective bulbs only. Great job segmenting the market there, people.

[Innovelli](https://inovelli.com/z-wave-vs-zigbee-vs-bluetooth-vs-wifi-smart-home-technology/) and [Tom’s Guide](https://www.tomsguide.com/us/smart-home-wireless-network-primer,news-21085.html
) offers a great primer on the different wireless technologies, though I have some straightforward advice for the consumer: __*don’t worry about using more than one wireless standard in your home.*__ Though there are issues with Zigbee, there are workarounds. I think it’s inevitable to use more than one standard to avoid limiting your options.

In the three-story home I set up, I have Zigbee light bulbs and door sensors, Z-Wave Plus motion sensors and outlets, and Lutron Caseta light switches. It was a matter of convenience, cost, and availability that I ended up using three standards, but surprisingly I have no issues with range or connectivity. I soon learned that is not always the case, especially with Zigbee network interference.

In another house I outfitted with Zigbee bulbs and Z-Wave motion sensors, I crammed all my network and connected devices onto a cheap server rack. This included a Wi-Fi mesh point, network switch, laptop, USB hard drive, Raspberry Pi, and SmartThings -- basically a Wi-Fi disaster. SmartThings was working initially, but then the Zigbee network started to fail. It happened once every few weeks, then every week, and then stopped working altogether. The Z-Wave devices continued to work without any problems, so I assumed issue was Zigbee, and not necessarily SmartThings. I simply moved the SmartThings hub away from the other Wi-Fi devices and the Zigbee lights started working again.

So the lesson I learned is: Zigbee network interference is real, and varies by setup. Physically move the Zigbe hub if you run into this issue.

In my search for deals on smart devices, I’ve noticed the following trends:

- The highest-reviewed motion sensors available today are usually Z-Wave. 
- The cheapest contact sensors are Zigbee, but new ones are hard to find. Z-Wave sensors tend to be 1.5 to 2x higher in price, but the difference is negligible—about $5-10 more per device.
- The cheapest and most readily available smart bulbs are Zigbee bulbs. Colored bulbs are expensive, no matter what standard it is.
- Zigbee and Z-Wave Plus power outlets are around the same price, though there are less Zigbee outlets available.
- Light switches usually use Z-Wave, but I strongly urge you to consider Lutron Caseta switches.

### Considerations before choosing a wireless standard

<ul class="alt">
<li><strong>The total number of connected devices you plan to have.</strong> Z-Wave device limit is 255. Zigbee is much higher at 65,355. Most homes will likely never hit Zigbee limits.</li>
<li><strong>The placement of the hub, and powered repeaters.</strong> Will you have enough repeaters to reach the furthest device? Z-Wave can hop on at most 4 always-powered devices.</li>
<li><strong>Philips Hue and its incompatible Zigbee standard.</strong> Philips Hue uses Zigbee but uses a different profile called ZLL.  Hue bulbs act as repeaters for Hue bridge only.</li>
<li><strong>Wireless communications can be slow.</strong> There is a noticeable delay between the sensor registering a change, sending data to the hub, running automation, turning on a light. I’ve noticed a 1-2 second delay.</li>
</ul>

### What you get with a smart home wireless standard
<ul class="alt">
<li>A dedicated wireless network for your sensors and lights that hopefully doesn’t interfere with existing wireless tech like Wi-Fi.</li>
</ul>

### Recommended Reading

<ul class="alt">
<li>Articles about wireless Home Standards from <a href="https://www.tomsguide.com/us/smart-home-wireless-network-primer,news-21085.html">Tom's Guide</a> and <a href="https://inovelli.com/z-wave-vs-zigbee-vs-bluetooth-vs-wifi-smart-home-technology/">Innovelli</a></li>
<li>Wirecutter article on <a href="https://thewirecutter.com/reviews/building-a-smart-home-with-apples-homekit/">Apple Homekit</a></li>
</ul>


<!-- Product Review section -->
<hr class="minor" />

![Z-Wave](assets\images\logo\zwave.jpg){:.image.dan-left}

## Z-Wave Plus

**If I had to choose one standard, I would hesitantly recommend Z-Wave Plus because new Z-Wave products are being released and readily available on the market.** I hesitate because reliable Z-Wave devices are hard to find—just look at 3-star Amazon reviews when you search for “Z-Wave.” The same can be said for Zigbee devices, depending on the category.

Theoretically, Z-Wave is better than Zigbee in most cases because it operates on a different, less congested wireless frequency. This reduces the chance of interference caused by other devices sharing the same frequency—a problem that Zigbee devices face with Wi-Fi devices using the same 2.4ghz frequency. Z-Wave’s hop (4) and device limit (255) look  bad compared to Zigbee (65,355), though I bet most homes will never hit this limit. 

### The Problems
Z-Wave Plus should be winning the wireless smart home standard, but it’s not. Z-Wave devices are more expensive than Zigbee counterparts, likely due to licensing and certification costs. Certification doesn’t necessarily guarantee quality, and the number of issues reported on Z-Wave devices is just too high for me to consider it a reliable standard. Here’s hoping that its successor, Z-Wave Plus, doesn’t repeat the same mistakes.


<!-- Product Review section -->
<hr class="minor" />

## The Competition

<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\logo\zigbee.png" alt=""/>
        <figcaption></figcaption>
      </figure>
      <h3>Zigbee</h3>
      <p>I've done testing in multiple houses, and I can confirm Zigbee network interference is real and a noticeable issue. But don't throw away your Zigbee light bulbs yet, because there is a simple solution: <i>keep your Zigbee hub at least five feet away from any router or Wi-Fi mesh point. Three meters is optimal, but five feet worked for me.</i> This is based off my personal experience fixing the Zigbee network, which used to go offline every few days.</p>

      <p>The Zigbee radio, whether it is built inside SmartThings, Hubitat, or a USB device, needs to stay away from other Wi-Fi devices (especially routers or Wi-Fi mesh points) because it uses the same 2.4ghz frequency as the router (which uses 2.4ghz or 5ghz). For anyone who recently purchased the latest SmartThings or Hubitat hub, then this is not a problem as those devices have Wi-Fi built-in, but I have the older, wired SmartThings hub and had to keep it wired to the Wi-Fi mesh point. My Zigbee network was offline for days, until I figured this out.</p>
    </div>
    <div class="6u$ 12u$(small)">
        <figure class="align-left">
          <img src="assets\images\logo\thread02.png" alt=""/>
        <figcaption>
    
        </figcaption>
        </figure>
    	<h3>Thread, Homekit, Wemo, Kasa</h3>
    	<p>There are new standards like Homekit, Thread, or WiFi-based ones like Wemo, but adoption rates remain low and I have concerns about the longevity of these standards. Homekit is slowly growing its footprint, but it is not usable outside Apple devices or even the iOS ecosystem. Be especially wary of any Wi-Fi labeled products from D-Link, TP-Link Kasa or Belkin Wemo as those are not open standards and may not be supported if the company shuts down. </p>
    </div>
</div>







