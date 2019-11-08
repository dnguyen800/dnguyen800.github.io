---
layout: page
title: Motion Sensors
short_title: motion-sensor
update: "<strong>August 16, 2019:</strong> The Bosch Zigbee motion sensor is massive in size, but it is cheap and works. Buy one already!"
competitors: "Dome, Zooz, Monoprice, SmartThings, Bosch, Ecolink, GE, Fibaro, Besense, Aeon Labs"
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
| ![](assets\images\logo\dome.png){:.image.logo} |  ![](assets\images\logo\zooz.png){:.image.logo} | ![](assets\images\logo\ge.png){:.image.logo}
|:-:|:-:|:-:
|**Z-Wave Plus Motion Sensor (DMMS1)** | **Z-Wave Plus Motion Sensor (ZSE18)** | **GE Z-Wave Plus Smart Motion Sensor (34193)** 

|---
| ![](assets\images\logo\ecobee.png){:.image.logo} | ![](assets\images\logo\bosch.png){:.image.logo} 
|:-:|:-:
| **Room Sensors** | **PIR Pet Immune Motion Sensor  (ISW-ZPR1-WP13)**

## What you need to know

I’m very surprised at the lack of quality motion sensors on the market today. A quick glance through [Amazon](https://www.amazon.com/s?k=z-wave+motion+sensor&ref=nb_sb_noss_2) shows only three motion sensors with 4-star ratings—the rest fail to make the cut. It must be difficult to make a reliable sensor with good battery life and USB charging capability . Motion sensors aren't cheap either—having to pay $35-40 adds up quickly for a basic but necessary sensor in your smart home.

With these high prices, I always remind people to think of alternatives, like installing simple motion-sensing light switches where possible. Not only are they significantly cheaper, but they double as a light switch and motion sensor. Guest bathrooms, closets, garage, and pantry areas make the most sense for motion-sensing switches.  See section: [Simple Lighting](simple-lighting.html) for details.

I’ve tested a few motion sensors and I found a few that I can recommend. Most of the sensors are **Z-Wave Plus** sensors, which is also my recommended wireless standard. I can’t promise you that the ones listed are the best sensors out there, but I can promise they are good for specific scenarios.

### Considerations before buying a motion sensor

<ul class="alt">
  <li><strong>Read reviews before buying a motion sensor.</strong> Common issues I've found in reviews include: pairing issues and sensors disconnecting from the hub after a period of time.</li>
  <li><strong>The response from a motion sensor response is not fast, at all</strong>. It takes about two seconds for the sensor's light to blink upon detection. It is even faster if the home automation hub, automations and sensors process locally on the network instead of the cloud.</li>
  <li><strong>Thoroughly test sensors and isolate failures in your automations.</strong> It’s possible to receive defective sensors.</li>
  <li><strong>Check that the sensor's battery type is a common one.</strong> My sensors all use CR123 batteries, though yours may be different.</li>
</ul>

### What you get with a motion sensor

<ul class="alt">
  <li>Lighting that turns on as you walk around the house.</li>
  <li>Lights remain on as long as a room is occupied.</li>
  <li>Create a DIY alarm system using motion and door sensors.</li>
</ul>


### Recommended Reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2WE1tgG">Dome Z-Wave Plus motion sensor</a> on Amazon.</li>
  <li>Purchase the <a href="https://www.thesmartesthouse.com/products/zooz-z-wave-plus-motion-sensor-zse18-with-magnetic-base-battery-or-usb-power">Zooz ZSE18 motion sensor</a> from The Smartest House.</li>
  <li>Purchase the <a href="https://www.mydigitaldiscount.com/bosch-security-motion-sensor-pir-pet-immune-for-samsung-smartthings-and-other-smart-hubs-with-zigbee-wireless/">Bosch Zigbee PIR motion sensor</a> from MyDigitalDiscount.</li>
  <li> Find the <a href="https://www.ebay.com/sch/i.html?_from=R40&_trksid=m570.l1313&_nkw=ge+z-wave+motion+sensor&_sacat=0&LH_TitleDesc=0&_osacat=0&_odkw=ge+z-wave+motion">GE Z-Wave Plus motion sensor</a> on eBay.</li>
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


## Dome Home Automation Z-Wave Plus Sensor (DMMS1) 

**My first motion sensor was the [Dome Home Automation Z-Wave Plus](https://amzn.to/2WE1tgG) sensor ``(DMMS1)``, and I can say it is the most reliable motion sensor I used and repurchased over the years.** I use them in stairways, hallways, entrances—mainly low to medium traffic areas where I absolutely need the light to turn on. Walking down the stairs in the dark shouldn’t happen in a smart home and Dome motion sensors haven’t failed me in this regard.

The detection range is better than most sensors, with objects reliably detected at 30 feet, and even further using higher sensitivities (and likely more false positives). In the living room, I use one sensor to detect someone entering from the opposite end of the room—about 30 feet. With the magnetic circular design, I can aim the sensor at any angle, which is perfect for stairways.

The sensors can’t be powered by micro-USB, so I don’t use them in high-traffic areas that will drain batteries quickly. I don’t have battery life benchmarks, but in real use, I change batteries every 3 to 6 months in medium traffic areas. 

### The Problems

The design of the base makes it impossible to mount on wall corners, so I place them right above the door or on a bookshelf for similar coverage. The lack of a micro USB port is disappointing and I hope the next revision includes one.

It is a Z-Wave Plus sensor, which has problems pairing to home automation hubs. Over the course of pairing and unpairing Dome sensors on different hubs for testing, I've run into pairing issues that magically resolved by repeating the same pairing steps over and over, like an insane person.  Once you pair this sensor to your hub, I recommend keeping it that way. 

### Installation and Smart Home Integration

Right out of the box, Dome sensors can be paired with SmartThings and Home Assistant, but sensitivity settings cannot be adjusted without installing the <a href="https://community.smartthings.com/t/release-dome-motion-sensor-official/78092">SmartThings custom device handler</a> created by user @krlaframboise. 

Pairing in Home Assistant is messy, as the sensor adds motion and ambient light entities, and some other values I’m not sure what to do with, like **``Burglar``**, **``Alarm Level``**, and so on. Motion detected is represented as a number value, rather than a binary value, so you would need to create a [``template sensor``](https://www.home-assistant.io/components/template/) to simplify things.

<hr class="major" />
<figure class="align-left">
       <img src="assets\images\product-photo\bosch-motion.png" alt=""/>
       <figcaption>
         The Bosch ISW-ZPR1-WP13 sensor. <strong>| Bosch</strong>
       </figcaption>
</figure>

## Bosch Zigbee PIR Motion Sensor (ISW-ZPR1-WP13)

**I bought the [Bosch Zigbee PIR motion sensor](https://www.mydigitaldiscount.com/bosch-security-motion-sensor-pir-pet-immune-for-samsung-smartthings-and-other-smart-hubs-with-zigbee-wireless/) on a whim, but it left an overall positive impression with its low price and...well, that it works without major issues.** If you need a cheap motion sensor and don't mind installing a SmartThings device handler, then I would recommend one to play around with. I use my Bosch sensor at the top of the stairs due to the sensor's narrow range. Normally this isn't a good quality for a motion sensor, but when other motion sensors accidentally activate when I'm walking in the hallway, these Bosch sensors are perfect as it only activates when I use the stairs. They're great for narrow spaces like hallways and stairways, but maybe not so great for open areas.

I was hoping that the response time of a Zigbee motion sensor would be lightning quick, but it is about the same as the Z-Wave motion sensors I've tested--it takes around 2-3 seconds to register motion and turn on a light. It's not great, but still usable. 

If not for the low price of these sensors, I wouldn't recommend these sensors due to the limitations I mentioned. But keep in mind that Z-Wave motion sensors cost $30-40 each! Motion sensors are a necessary device to keep track of house activity and automate lighting, so any working sensor under $15 is worth checking out.

### The Problems
If you thought the sensor looked large from the photo, then you'll be surprised to know that the Bosch sensor is even bigger in person. It is the largest motion sensor in existence and looks like a relic from the 90's. Part of the reason for the large size is the 4 AA batteries required to power the thing. Does that mean the sensor will last for six years according to this [post](https://community.smartthings.com/t/bosch-security-pir-pet-immune-motion-sensor-12-w-free-shipping/126143)? After a month of testing, I'm not so sure. I use the sensor in a high-traffic stairway (about 50 detections/day) with four worn Eneloop rechargeable batteries and the battery life currently stands at 56%. These aren't ideal testing conditions, but I wouldn't expect the batteries to last longer than a year.

There is a 3-minute delay after each detection, meaning motion isn't registered by the sensor until three minutes have passed. The delay is hard-coded in the sensor and cannot be changed. This has never been a problem with my lighting automations as I keep lights on for at least five minutes before turning off, but may be a deal breaker for you.

Installation with SmartThings is not possible out-of-the-box, which I'll go into detail below.

### Installation and Smart Home Integration
SmartThings installation requires a custom device handler provided by user [@tomasaxerot](https://github.com/tomasaxerot/SmartThings/blob/master/devicetypes/tomasaxerot/bosch-motion-detector.src/bosch-motion-detector.groovy), which you should already be familiar with as a SmartThings user. Using a custom device handler forces SmartThings to communicate by cloud instead of local, but I've read online that changing the sensor's Device Type setting  in SmartThings's IDE to 'smartsense motion sensor' will allow the sensor to process locally and improve automation speed, though I haven't noticed any significant improvements.

The sensor works with Home Assistant (according to this [post](https://community.home-assistant.io/t/bosch-isw-zpr1-wp13/48054/10)), but your mileage may vary. I've always had good luck with pairing Zigbee devices using Home Assistant's new Zigbee management panel, so I'll test the sensor soon and report back.


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
      <p>If a sensor only works 90% of the time, is it worth buying? <strong>The <a href="https://www.thesmartesthouse.com/products/zooz-z-wave-plus-motion-sensor-zse18-with-magnetic-base-battery-or-usb-power">Zooz Z-Wave Plus Motion Sensor</a> (ZSE18) is one of the cheapest motion sensors on the market ($20-23) but after testing for months and running into several issues, I can’t recommend these for any use.</strong>  With a reduced range (around 15-20ft) and less than 100% reliability, I can’t use the sensor in areas where I absolutely need the light to turn on, so I relegated it to less critical areas like the bedroom or office. If I could return them, I would and purchase some reliable sensors instead.</p>

<p>Out of all that I’ve tested, this sensor’s design is my favorite. It uses a magnetic base like the Dome sensors, but has the micro-USB port accessible from the outside of the case. This lets me position the sensor in a way that doesn’t create tension on the cable and keep the sensor steady.</p>
<h4>The Problems</h4>
<p>My first batch of sensors turned out to be faulty—the default sensitivity settings were way too low to be useful in any scenario. Luckily, I received a replacement but the sensors continue to exhibit different issues. 10% of the time, the motion sensor reports active motion but remains as active indefinitely, which breaks my lighting automations and keeps the lights on. Once I walk by the sensor, it reports active motion again, though it has already been reporting active for several hours! The same issue happens with reporting inactive motion, though the issue is fixed by walking near the sensor and waking it up. My theory is that the sensor goes into sleep mode, but forgets to update status before doing so. It’s a frustrating hardware flaw that is unlikely to be fixed.</p>
<h4>Installation and Smart Home Integration</h4>
<p>Connecting to SmartThings is hit-or-miss for me. I’m never able to pair the sensor on the first try. I have also had to reconnect the sensor to SmartThings once a month, on average.</p>
   </div>


   <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\ge-motion-sensor.jpg" alt=""/>
        <figcaption> GE motion sensor <strong>| GE</strong></figcaption>
      </figure>
      <h3>GE Z-Wave Plus Motion Sensors</h3>
      <p><strong>I continue to buy <a href="https://www.ebay.com/sch/i.html?_from=R40&_trksid=m570.l1313&_nkw=ge+z-wave+motion+sensor&_sacat=0&LH_TitleDesc=0&_osacat=0&_odkw=ge+z-wave+motion">GE Z-Wave Plus Motion Sensors</a> for its excellent range and USB power, but since it’s no longer being sold at retailers, I can’t recommend it.</strong> I sometimes find deals on eBay for under $30, which is a fair price as the sensor isn’t perfect (poor battery life and limited mounting options come to mind). These sensors are great in high traffic and medium-sized rooms, but only if you can power the sensors with a USB cable.</p>

       <figure class="align-center" style="width: 50%;">
       <a class="image-link" href="assets\images\other\motion-sensor-range.jpg" ><img src="assets\images\other\motion-sensor-range.jpg" alt="" /></a>
       <figcaption>
          The detection range for most motion sensors. <strong>| GE</strong>
       </figcaption>
       </figure>

<p>I can vouch that the range is really good, around 35 to 40 feet. I use these sensors in the living room and dining room and it always detects motion as expected, whether in light or darkness. The response is not instant—I experience about a 1-2 second lag from detecting motion to turning on the light. If you’re running around the house in the dark, you will definitely outrun the light automations.</p>
<p>This sensor works best on a level surface and can't be angled up or downwards easily, making it unsuitable for stairways.  Motion detection below the sensor's field of view is also limited, so it's best to place the sensor at a height above the waist. I think it is best used to detect presence in medium-size rooms, when placed on a shelf, side table or TV stand.</p>
<h4>Installation and Smart Home Integration</h4>
<p>Pairing in SmartThings is easy, but Home Assistant is a little more difficult as it creates five entities (though only one is useful) and spits out number values instead of an on/off value. I ended up creating a template sensor to simplify automations.</p>
   </div>
   <div class="6u$ 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\besense.jpg" alt=""/>
        <figcaption>
         The BeSense Ceiling motion sensor. <strong>| BeSense</strong>
        </figcaption>
        </figure>
    	<h3>BeSense Ceiling Motion Sensor</h3>
    	<p>The <a href="https://amzn.to/2GKbwLr">BeSense ceiling motion sensor</a> is a new sensor on the market that caught my eye on Amazon. I haven’t tested it, but the good reviews, use of AA batteries and affordable price made me curious. It is a ceiling sensor so it is best used in small rooms, hallways, and condos where the ceiling isn’t so high. If I ever buy it, I’ll report my findings here. </p>
    </div>
   <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\ecobee-sensor.png" alt=""/>
        <figcaption>Ecobee temp sensors. <strong>| Ecobee</strong></figcaption>
      </figure>
      <h3>Ecobee Sensors</h3>
      <p><strong>Ecobee thermostats come with room sensors that monitor temperature, but did you know that it can also be used as a motion sensor?</strong> I would never buy purchase <a href="https://amzn.to/2PDNrK2">Ecobee sensors</a> as dedicated motion sensors, but they are nice to have as secondary sensors to confirm if a room is truly empty.</p>

<p>Some important info about the sensors: they can be used only if you have an Ecobee thermostat installed as it uses a proprietary method to communicate. The sensor’s battery can last for over a year using a single CR2032 battery—the same ones used in most car key fobs. </p>
<h4>The Problems</h4>
<p>Motion detection is not timely, at all. It takes more than several minutes to report occupancy, and an empty room. I couldn’t think of many useful automations using this as a motion sensor, except as additional confirmation that no one is present in a room. </p>
<h4>Installation and Smart Home Integration</h4>
<p>If you integrate the Ecobee thermostat with Smartthings or Home Assistant, then these sensors are automatically added to your setup. </p>
   </div>

   

</div>