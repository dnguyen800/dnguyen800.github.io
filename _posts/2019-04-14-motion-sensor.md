---
layout: page
title: Motion Sensors
short_title: motion-sensor
excerpt: Kind of like a camera (but less creepy). 
competitors: "Dome, Zooz, Monoprice, SmartThings, Ecolink, GE, Fibaro, Besense, Aeon Labs"
permalink: /motion-sensor
image: assets/images/overlay-ws/sensors.jpg
image_credit: Dan Nguyen
categories: 
    - "Sensor"
    - "Security"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\dome.png){:.image.logo} |  ![](assets\images\logo\zooz.png){:.image.logo} | ![](assets\images\logo\ge.png){:.image.logo} | ![](assets\images\logo\ecobee.png){:.image.logo} 
|:-:|:-:|:-:|:-:
|**Z-Wave Plus Motion Sensor (DMMS1)** | **Z-Wave Plus Motion Sensor (ZSE18)** | **GE Z-Wave Plus Smart Motion Sensor (34193)** | **Room Sensors**


## What you need to know

I’m very surprised at the lack of quality motion sensors on the market today. A quick glance through [Amazon](https://www.amazon.com/s?k=z-wave+motion+sensor&ref=nb_sb_noss_2) shows only three motion sensors with 4-star ratings—the rest don’t make the cut. It seems hard to make a reliable sensor with good battery life and USB charging capability. It’s not cheap either—having to pay $35-40 adds up quickly for a basic but necessary sensor in your smart home.

With these high prices, I always remind people to think of alternatives, like installing simple motion-sensing light switches where possible. Not only are they significantly cheaper, but they double as a light switch and motion sensor. Guest bathrooms, closets, garage, and pantry areas make the most sense for these switches.  See section: [Simple Lighting](simple-lighting.html).

I’ve tested a few motion sensors and I found a few that I like. All of them happen to be **Z-Wave Plus** sensors, which is also my recommended wireless standard. I can’t promise you that the ones listed are the best sensors out there, but I can promise they are good for specific scenarios.

### Considerations before buying a motion sensor

<ul class="alt">
  <li><strong>Read reviews before buying.</strong> Common issues with pairing and disconnecting from the hub.</li>
  <li><strong>Motion sensor response is not instant</strong>—it takes about two seconds for the light to turn on from a detection.</li>
  <li><strong>Thoroughly test sensors and isolate failures in your automations.</strong> It’s possible to receive defective sensors.</li>
  <li><strong>Check that the battery type is common.</strong> My sensors all use CR123 batteries, though yours may be different.</li>
</ul>

### What you get with a motion sensor

<ul class="alt">
  <li>Lighting that turns on as you walk around the house.</li>
  <li>Lights remain on as long as a room is occupied.</li>
</ul>


### Recommended Reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2ImGlID">Dome Z-Wave Plus motion sensor</a> on Amazon</li>
  <li>Amazon search for <a href="https://www.amazon.com/s?k=z-wave+motion+sensor&ref=nb_sb_noss_2">Z-Wave motion sensors</a>.</li>
  <li>Connect the Dome Z-Wave motion sensor to SmartThings with this <a href="https://community.smartthings.com/t/release-dome-motion-sensor-official/78092">device handler</a>.</li>
</ul>

<hr class="major" />

<figure class="align-left">
       <img src="assets\images\product-photo\dome-motion-sensor.jpg" alt=""/>
       <figcaption>
         The DMMS1 sensor. <strong>| Dome</strong>
       </figcaption>
</figure>

## Dome Home Automation Z-Wave Plus (DMMS1) sensor

**My first motion sensor was the Dome Home Automation Z-Wave Plus ``(DMMS1)`` sensor, and I can say it is the most reliable motion sensor I used and repurchased over the years.** I use them in stairways, hallways, entrances—mainly low to medium traffic areas where I absolutely need the light to turn on. Walking down the stairs in the dark shouldn’t happen in a smart home and Dome motion sensors haven’t failed me in this regard.

The detection range is better than most sensors, with objects reliably detected at 30 feet, and even further using higher sensitivities (and likely more false positives). In the living room, I use one sensor to detect someone entering from the opposite end of the room—about 30 feet. 

The sensors can’t be powered by micro-USB, so I don’t use them in high-traffic areas that will drain batteries quickly. I don’t have battery life benchmarks, but in real use, I change batteries every 3 to 6 months in medium traffic areas. 

### The Problems

The design of the base makes it impossible to mount on wall corners, so I place them right above the door or on a bookshelf for similar coverage. 

### Installation and Smart Home Integration

Right out of the box, Dome sensors can be paired with SmartThings and Home Assistant, but sensitivity settings cannot be adjusted without installing the <a href="https://community.smartthings.com/t/release-dome-motion-sensor-official/78092">SmartThings custom device handler</a> created by @krlaframboise. 

Pairing in Home Assistant is messy, as the sensor adds motion and ambient light entities, and some other values I’m not sure what to do with, like **``Burglar``**, **``Alarm Level``**, and so on. Motion detected is represented as a number value, rather than a binary value, so you would need to create a **``template sensor``** to simplify things.

<!-- Competition section -->
<hr class="minor" />

## The Competition

<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\zooz.png" alt=""/>
        <figcaption>The ZSE18 sensor. <strong>| Zooz</strong></figcaption>
      </figure>
      <h3>Zooz Z-Wave Plus Motion Sensor (ZSE18)</h3>
      <p>If a sensor only works 90% of the time, is it worth buying? <strong>The Zooz Z-Wave Plus Motion Sensor (ZSE18) is one of the cheapest motion sensors on the market ($20-23) but after testing for months and running into several issues, I can’t recommend these for any use.</strong>  With a reduced range (around 15-20ft) and less than 100% reliability, I can’t use the sensor in areas where I absolutely need the light to turn on, so I relegated it to less critical areas like the bedroom or office. If I could return them, I would and purchase some reliable sensors instead.</p>

<p>Out of all that I’ve tested, this sensor’s design is my favorite. It uses a magnetic base like the Dome sensors, but has the micro-USB port accessible from the outside of the case. This lets me position the sensor in a way that doesn’t create tension on the cable and keep the sensor steady. </p>

<h4>The Problems</h4>
<p>My first batch of sensors turned out to be faulty—the default sensitivity settings were way too low to be useful in any scenario. Luckily, I received a replacement but the sensors continue to exhibit different issues. 10% of the time, the motion sensor reports active motion but remains as active indefinitely, which breaks my lighting automations and keeps the lights on. Once I walk by the sensor, it reports active motion again, though it has already been reporting active for several hours! The same issue happens with reporting inactive motion, though the issue is fixed by walking near the sensor and waking it up. My theory is that the sensor goes into sleep mode, but forgets to update status before doing so. It’s a frustrating hardware flaw that is unlikely to be fixed.</p>

<h4>Installation and Smart Home Integration</h4>
<p>Connecting to SmartThings is hit-or-miss for me. I’m never able to pair the sensor on the first try. I have also had to reconnect the sensor to SmartThings once a month, on average.</p>
   </div>


   <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\ge-motion-sensor.jpg" alt=""/>
        <figcaption> GE motion sensor | GE</figcaption>
      </figure>
      <h3>GE Z-Wave Plus Motion Sensors</h3>
      <p><strong>I continue to buy GE Z-Wave Plus Motion Sensors for its excellent range and USB power, but since it’s no longer being sold at retailers, I can’t recommend it.</strong> I sometimes find deals on eBay for under $30, which is a fair price as the sensor isn’t perfect (poor battery life and limited mounting options come to mind). These sensors are great in high traffic and large areas, but only if you can power the sensors with a USB cable.</p>

       <figure class="align-center" style="width: 50%;">
       <a class="image-link" href="assets\images\other\motion-sensor-range.jpg" ><img src="assets\images\other\motion-sensor-range.jpg" alt="" /></a>
       <figcaption>
          The detection range for most motion sensors. <strong>| GE</strong>
       </figcaption>
       </figure>

<p>I can vouch that the range is really good, around 35 to 40 feet. I use these sensors in the living room and dining room and it always detects motion as expected, whether in light or darkness. The response is not instant—I experience about a 1-2 second lag from detecting motion to turning on the light. If you’re running around the house in the dark, you will definitely beat the lights. </p>

<h4>Installation and Smart Home Integration</h4>
<p>Pairing in SmartThings is easy, but Home Assistant is a little more difficult as it creates five entities (though only one is useful) and spits out number values instead of an on/off value. I ended up creating a template sensor to simplify automations.</p>
   </div>
   <div class="6u$ 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\besense.jpg" alt=""/>
        <figcaption>
         Ceiling motion sensor. | BeSense
        </figcaption>
        </figure>
    	<h3>BeSense Ceiling Motion Sensor</h3>
    	<p>The BeSense ceiling motion sensor is a new sensor on the market that caught my eye on Amazon. I haven’t tested it, but the good reviews, use of AA batteries and affordable price made me curious. It is a ceiling sensor so it is best used in small rooms, hallways, and condos where the ceiling isn’t so high. If I ever buy it, I’ll report my findings here. </p>
    </div>
   <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\ecobee-sensor.png" alt=""/>
        <figcaption>Ecobee temp sensors. | Ecobee</figcaption>
      </figure>
      <h3>Ecobee Sensors</h3>
      <p><strong>Ecobee thermostats come with room sensors that monitor temperature, but did you know that it can also be used as a motion sensor?</strong> I would never buy purchase Ecobee sensors as dedicated motion sensors, but they are nice to have as secondary sensors to confirm if a room is truly empty.</p>

<p>Some important info about the sensors: they can be used only if you have an Ecobee thermostat installed as it uses a proprietary method to communicate. The sensor’s battery can last for over a year using a single CR2032 battery—the same ones used in most car key fobs. </p>

<h4>The Problems</h4>
<p>Motion detection is not timely, at all. It takes more than several minutes to report occupancy, and an empty room. I couldn’t think of many useful automations using this as a motion sensor, except as additional confirmation that no one is present in a room. </p>

<h4>Installation and Smart Home Integration</h4>
<p>If you integrate the Ecobee thermostat with Smartthings or Home Assistant, then these sensors are automatically added to your setup. </p>
   </div>

   

</div>