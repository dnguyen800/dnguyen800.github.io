---
layout: page
title: Contact Sensors
short_title: contact-sensor
excerpt: Contact sensors tell you when your doors are open or closed--which is important, right?
permalink: /contact-sensor
competitors: "Dome, Monoprice, Visonic, SmartThings, Ecolink, Aeon Labs, and no-name brands."
image: assets/images/overlay-ws/contact-sensor.jpg
image_credit: Dan Nguyen
categories: 
    - "Sensor"
    - "Security"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\dome.png){:.image.logo} |  ![](assets\images\logo\monoprice.png){:.image.logo} | ![](assets\images\logo\visonic.png){:.image.logo} | ![](assets\images\logo\konnected.png){:.image.logo} 
|:-:|:-:|:-:|:-:
|**Z-Wave Plus Door Sensors (DMWD1)** | **Z-Wave Plus Door Sensor, No Logo** | **Door Sensor (MCT-340E)** | **Konnected Alarm Panel**

##  What you need to know

Contact sensors consist of two pieces: a magnet piece, and a piece that holds the wireless radio that communicates to the hub. Sensors are incredibly easy to install on doors and windows—just mount the pieces next to each other on a flat surface.  There is usually a gap between the door and door frame, but some sensors allow for a gap as large as one inch (check your product details). 

It seems like door sensors are the easiest to get right, as all of my sensors work as expected without any disconnect issues. Even the cheapest sensors work reliably. Still, I’ve noticed whenever SmartThings notifies me of opened doors, there may be a several minute delay. I don’t think it is a sensor issue, but an issue with Android’s battery saver function. 

Some sensors handle this better than others, but the sensitivity of door sensors is quite low—so the door can be slightly open, but the sensor reports it as closed. I tried using a sensor on a refrigerator door, but it failed to report the door as open when the door was open by as much as one-fourth of an inch. Needless to say, the electricity bill did not go down that month.

I have my recommendation of contact sensors listed below, but there are plenty of sensors out there that work just fine and are probably cheaper. 

### Considerations before buying a door sensor

<ul class="alt">
  <li><b>When installing the sensor, don’t place it on the door where the battery cover is blocked.</b> </li>
  <li><b>Select a contact sensor that uses a battery type you commonly have.</b> Monoprice uses AAA batteries, Dome is CR14250 (rare), and Visonic is CR2032.</li>
</ul>


### What you get with a door sensor

<ul class="alt">
  <li>Know when people arrive or leave home. The lights can turn on right as you open the front door. </li> 
  <li> Use the sensors as a part of a DIY security system.</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li>Purchase the <a href="https://www.monoprice.com/product?p_id=24259">Monoprice door sensors</a> on Monoprice and Konnected board from <a href="https://konnected.io/">Konnected.io</a></li>
  <li><b>Affiliate link:</b> Purchase the <a href="https://amzn.to/2IDJRwF">Visonic door sensor</a> or <a href="https://amzn.to/2Kjr254">Dome Door Sensor</a> on Amazon</li>
  <li> SmartThings custom device handlers for <a href="https://community.smartthings.com/t/release-dome-door-sensor-official/76321">Dome door sensors</a></li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
       <img src="assets\images\product-photo\dome-door-sensor.jpg" alt=""/>
       <figcaption>
         What's up with the weird battery size? <b>| Dome</b>
       </figcaption>
</figure>

## Dome Z-Wave Plus Door Sensors (DMWD1) 

I was able to snag the [Dome Z-Wave Plus Door Sensors](https://amzn.to/2Kjr254) (DMWD1) during a sale from domeha.com and it was a good purchase at the time. **But no matter how good the Dome DMWD1 sensor is, the irregular battery size is a huge drawback as no one wants to buy a pair of batteries for one device.** Heck, it even uses a different battery size than the Dome motion sensor (CR123A)! I prefer a lower cost than smaller sensor size, and I would have not purchased this if I had paid more attention to the battery size.

### The Problems

I’ll bring up the issue with the [odd battery size (CR14250)](https://www.amazon.com/s?k=CR14250&ref=nb_sb_noss_2) again, because in a market with reliable contact sensors, I can find a reliable sensor that uses a common battery size. Right now, I use these sensors on windows that are rarely opened, so changing batteries won’t be an issue until a year or two from now. 

### Installation and Smart Home Integration

I used these sensors with SmartThings and a [custom device handler by user @krlaframboise](https://community.smartthings.com/t/release-dome-door-sensor-official/76321) and haven’t run into any issues with pairing or general use. Detection happens nearly instantly, though not noticeably faster or slower than the other sensors I used. The sensors include double-sided tape to easily mount on the door.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/dome-door-st.png"  />
      <figcaption>
         <b>SmartThings: Good</b><br>Using the free ST device handler adds more settings.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/dome-door-ha.png"  />
       <figcaption>
         <b>Home Assistant: Great</b><br>Creates one binary sensor entity in HA. 
       </figcaption>
      </figure>
	</div>
</div>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
       <img src="assets\images\product-photo\monoprice-door.jpg" alt=""/>
       <figcaption>
         <b>Z-Wave Plus Door Sensor | Monoprice</b>
       </figcaption>
</figure>
<p></p>

## Monoprice Z-Wave Plus Door Sensors (No Logo)

**The [Monoprice Z-Wave Plus Door Sensors](https://www.monoprice.com/product?p_id=24259) are a bit pricey, but they work as advertised and are a great way to use my spare AAA batteries.** The sensors won’t win any awards for design—these are the bulkiest door sensors I have and can be an eyesore. If you’re looking for hidden sensors, then look into Monoprice’s recessed sensors. Make sure not to buy the **``Stitch``** version (Monoprice’s new line of WiFi-based smart devices) as they are not compatible with any of the home automation hubs.

For $20, I was expecting a low-profile sensor, but the sensors are reliable at least and that is the most important aspect in a connected device.

### Installation and Smart Home Integration

The maximum gap between the sensor and magnet is 0.4”, which is slightly smaller than the other door sensors I tested. If you plan to use this sensor with the garage door, that is unlikely to go well without workarounds. 

Pairing the sensors is straightforward in SmartThings and Home Assistant so I won’t go over it here. There is a tamper switch located on the back of the sensor but is only usable with a [SmartThings device handler by user @rboy](https://community.smartthings.com/t/release-official-monoprice-z-wave-plus-sensor-door-window-mailbox-open-close-sensor-recessed-mounted-15268-15270-24259-with-external-trigger-option-and-tamper-device-handler/97273) that is locked behind a paywall. Device handlers are nice to have to access more details (like battery level), but not necessary.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/monoprice-door-st.png"  />
      <figcaption>
         <b>SmartThings: Good</b><br> Works. More settings in a paid device handler.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/monoprice-door-ha.png"  />
       <figcaption>
         <b>Home Assistant: Good</b><br> This is how a door sensor looks like in HA
       </figcaption>
      </figure>
	</div>
</div>
<p></p>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
       <img src="assets\images\product-photo\visonic-sensor.jpg" alt=""/>
       <figcaption>
         The MCT-340E sensor <b>| Visonic</b>
       </figcaption>
</figure>

## Visonic Door Sensor (MCT-340E) 

**I bought the [Visonic Door Sensor](https://amzn.to/2IDJRwF) (MCT-340E) on a whim because they were so cheap ($10), but the small profile, popular battery size (CR2032), and reliability convinced me that this would make a solid budget recommendation.** The sensor also monitors temperature, though I have never received an accurate reading. If you don’t have any issues with your Zigbee network, then I would recommend giving these sensors a try.

I have a Wi-Fi mesh network and a small Zigbee network of smart bulbs—both operating on the 2.4ghz frequency—but haven’t run into any connection issues. I would worry about connectivity in a much larger home, but for medium-sized homes and condos, range is not going to be a concern.

<p class="box">
<i>The sensor is $5 cheaper at <a href="https://www.mydigitaldiscount.com/visonic-mct-340-e-wireless-door-window-temperature-sensor-2.4ghz-zigbee-now-works-natively-with-samsung-smartthings-hub/">mydigitaldiscount.com</a>, where I originally bought it for $10.</i></p>

### Installation and Smart Home Integration

Pairing these sensors with Home Assistant can get a little messy as it creates multiple entities for the contact and temperature sensors, but pairing with SmartThings is simple. It is one reason I still recommend SmartThings over Home Assistant, where pairing devices is much more straightforward. 

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
       <img src="assets\images\product-photo\konnected.jpg" alt=""/>
       <figcaption>
         <b>| Konnected</b>
       </figcaption>
</figure>

## Konnected

If you already have wired sensors installed from a security system in your home, you should check out the [Konnected board](https://konnected.io/), which can reuse those sensors with home automation hubs like SmartThings, Home Assistant and Hubitat. I installed one at a friend’s house and was able to connect four door sensors, a siren, a piezo buzzer, and used the 12V port to power a wall-mounted tablet. Be warned that it is a product with bugs—I spent two days trying to figure out an issue that was eventually resolved with a firmware update.

The cost of a Konnected module ($89) is high, but when you factor in the cost of purchasing wireless sensors at $20-30 each, then the module pays for itself with five wired sensors. I also like the fact that I can use a Honeywell wired siren with Konnected because it’s much louder and effective at scaring off intruders than any wireless siren I’ve tried.

### Installation and Smart Home Integration

This is an advanced DIY installation and requires some study of your previous alarm system. Not every system is compatible, so it’s important to read through the Konnected Support section before purchasing. The Konnected Facebook group is also a friendly group to ask questions—I received responses within an hour of asking, though none of the advice solved my issue. Experience with electrical wiring, voltage, and a lot of patience is needed.


<div class="row">
	<!-- Break -->
	<div class="4u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/konnected-st.png"  />
      <figcaption>
        I frequent the Konnected status page in SmartThings for troubleshooting issues.
      </figcaption>
      </figure>
	</div>
	<div class="4u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/konnected-st-02.png"  />
       <figcaption>
         SmartThings Four Konnected sensors and a siren connected in ST.
       </figcaption>
      </figure>
	</div>
	<div class="4u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/konnected-st.png"  />
       <figcaption>
         What a Konnected sensor looks like in SmartThings.
       </figcaption>
      </figure>
	</div>
</div>