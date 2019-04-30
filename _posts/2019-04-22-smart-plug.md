---
layout: page
title: Smart Plugs
short_title: smart-plug
excerpt: Useful as a Z-Wave or Zigbee network extender, but not much more.
update: <strong>April 22, 2019:</strong> Added my review of smart plugs.
competitors: "Securifi, Monoprice, Belkin Wemo, TP-Link Kasa"
permalink: /smart-plug
image: assets/images/overlay-ws/smart-plug.jpg
image_credit: Dan Nguyen
categories: 
    - "Gadgets"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\securifi.png){:.image.logo} | ![](assets\images\logo\monoprice.png){:.image.logo}
|:-:|:-:
| **Peanut Plug (Zigbee)** | **Z-Wave Plus Smart Plug and Repeater with 2 USB Ports**<br>**Z-Wave Plus Wall Socket Plug-in**

## What you need to know

<strong>Before we get started, here's a word of advice about safety:</strong> think twice about the device you're connecting to a smart plug. Do you really want to connect an expensive TV or an electric car to a $10 plug? Is the plug even UL certified or is it an unknown brand sold on Amazon.com? I've read on forums of people connecting their Nissan Leaf chargers to a smart plug and burning out the plug, and outlet, luckily avoiding the house. What would happen to your house if the portable heater or curling iron connected to the smart plug failed to turn off? I've witnessed instances where the plug was reportedly off, but I saw with my own eyes that it was still on. Read through some 1-star reviews on Amazon to understand the risks of using cheap smart plugs with expensive or high voltage devices.

I've found that the best use of a smart plug is not as a smart plug, but as a range extender for your Z-Wave or Zigbee network. For that reason, I recommend avoiding Wi-Fi plugs as they lack this feature. I find smart plugs to be more of a hindrance than useful due to their bulky size, which blocks out one to three outlets on a surge protector or wall outlet. I use one-foot power extension cords from [Monoprice](https://www.monoprice.com/product?p_id=5297) to deal with that problem, but it doesn't make for a clean look.


<figure class="align-center" style="width: 50%;" >
 <img src="assets\images\other\smart-plug-use.jpg" />
 <figcaption>
An Ikea cable management/charger box can be paired with a smart plug to turn off at night, but the electricity saved is likely offset by the smart plug's electricity usage.
 </figcaption>
</figure>

Smart plugs work best with devices that have an **``always on``** setting. Floor lamps, garage lights, portable fans, multi-port USB chargers, coffee makers and humidifiers have dials or power switches so they turn on right away when plugged into an outlet. There are some devices that have issues when power is immediately cut off. Don't connect a Raspberry Pi or a computer to this, as it could lead to SD card corruption. 

I don't use smart plugs in any of my setups today because they failed to automate or simplify my tasks. For floor lamps, smart bulbs at least offer the option to automatically dim the lights according to the time. Smart plugs would only allow an on/off lighting automation. At best, I use the [Monoprice Z-Wave Plug](https://www.monoprice.com/product?p_id=35877) to power my camera and motion sensor with the built-in USB ports.


### Considerations before buying a smart plug
<ul class="alt">
  <li> A Wi-Fi based plug will not extend your Z-Wave or Zigbee network.</li>
  <li>DO NOT connect the smart plug to a high voltage device, like an electric car charger. Read the manual to confirm the max amperage, voltage, wattage the plug can handle. </li>
  <li>USB ports on smart plugs cannot be remotely turned on/off, unless specified.</li>
  <li>Avoid unknown brands from Amazon. They are usually not UL certified or RoHS compliant, and who knows what data is being transmitted by the plug and its mobile app.</li>
</ul>

### What you get with a smart plug
<ul class="alt">
  <li>A dedicated wireless repeater for your Z-Wave or Zigbee network.</li>
  <li>Some smart plugs monitor energy usage. Useful as an FYI.</li>
  <li>Remotely turn on/off one connected device, like a floor lamp.</li>
  <li>Some smart plugs provide USB ports for USB-powered motion sensors and cameras</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2Iz0Xhp">Securifi Peanut Plug</a> for Zigbee networks. Can set up with any Zigbee hub, not just Almond routers.</li>
  <li>Purchase the <a href="https://www.monoprice.com/product?p_id=35877">Monoprice Z-Wave Plus Plug</a></li>
  <li><a href="https://github.com/pakmanwg/smartthings-peanut-plug/blob/master/devicetypes/pakmanwg/peanut-plug.src/peanut-plug.groovy">SmartThings device handler</a></li>
</ul>


<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
  <img src="assets\images\product-photo\securifi-peanut.jpg" alt=""/>
  <figcaption>
    The Peanut plug. <strong>| Securifi</strong>
  </figcaption>
</figure>

## Securifi Peanut Plug

**The [Securifi Peanut plug](https://amzn.to/2Iz0Xhp) is a Zigbee smart plug that's designed to work with the Securifi Almond network router, but can connect to any Zigbee hub like Home Assistant and SmartThings using a [custom device handler](https://github.com/pakmanwg/smartthings-peanut-plug/blob/master/devicetypes/pakmanwg/peanut-plug.src/peanut-plug.groovy).** You do lose one functionality when connecting to an unofficial hub--the ability to measure energy readings from the device connected to the outlet.

I bought a Peanut plug at $10 because it was cheap and I wanted a reliable Zigbee network extender, but I have no other use for this smart plug. My floor lamps use smart bulbs and most of my devices need to be **``always-on``**.

The Peanut plug has a max limit of 15A, 1200W, or 1 HP. Please don't connect your portable heater or electric car charger to this.

I can't verify if these plugs actually increase the Zigbee network range, as I never had to deal with range issues. I'm going by the word of the [SmartThings community](https://community.smartthings.com/t/faq-which-devices-work-double-as-a-zigbee-extender-2018/143695) that it acts like it's supposed to. 

### The Problems

In terms of physical dimensions, it is a bit on the bulky side and will fall out of worn wall outlets. The best position for this plug is the top part of the wall outlet, though the plug may block some adapters connected to the the bottom outlet. This [website](https://www.simplysmart123.com/peanut-smart-plug-with-smartthings-and-alexa/) has useful side-by-side comparison of the plug and how it fits into an outlet.



### Installation and Smart Home Integration

Installation is a little more complicated as the Peanut plug wasn't designed for connecting to anything other than the Securifi Almond router. It requires adding a SmartThings device handler and using the SmartThings IDE to change device settings. A quick Google search will show several tutorials on how to do it, like this [one](https://www.instructables.com/id/Integrate-Peanut-Plug-With-SmartThings-Hub-Via-Sma/).

Pairing the Peanut plug with Home Assistant and a Zigbee USB device is straightforward. The plug shows up as a generic Zigbee plug.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/peanut-plug-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Easily pairs with Home Assistant as a generic Zigbee plug.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Good</strong><br>No native integration, but works through SmartThings or Home Assistant.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/securifi-peanut-st.png" />
      <figcaption>
      <strong>SmartThings: Good</strong><br>Requires custom device handler to set up.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/not_available.png" />
       <figcaption>
         <strong>Securifi App: N/A</strong><br>I did not test as I don't have the Almond router. </figcaption>
      </figure>
	</div>
</div>



<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
  <img src="assets\images\product-photo\monoprice-outlet02.png" alt=""/>
  <figcaption>
    The Z-Wave Plus Smart Plug/Repeater <strong>|  Monoprice</strong>
  </figcaption>
</figure>

## Monoprice Z-Wave Plus Smart Plug and Repeater with 2 USB Ports 

**The [Monoprice Z-Wave Plus Smart Plug](https://www.monoprice.com/product?p_id=35877) is more useful with the built-in USB ports, but I still hold the opinion that smart plugs are only useful if you need a Z-Wave network extender.** I purchased these plugs at $22 but they remain stored away in a box because I have yet to find a good use for them.

The build quality of the Monoprice plug is much better than the previous model, which was basically a pointy plastic enclosure. I like the rounded look of the plug, but it is still a bulky device. There is an LED light in the front that emits a pretty glow that becomes slowly annoying if the plug is in the bedroom. The included USB ports can be used to power Nest cameras or motion sensors, but cannot reliably power a Raspberry Pi 3B+ as that requires a proper 2.5A power supply. Not a charger.

One nifty feature that the plug has is the ability to detect electricity usage, though I don't know how accurate it is. If you're curious at how much electricity a device uses, then this is an easy way to monitor. I always assumed that any powered USB hub would be constantly draining electricity (called "vampire draw," ["standby power"](https://en.wikipedia.org/wiki/Standby_power)) when plugged in, but I was able to confirm my hub only draws power if a device is connected and charging through it. Cool! I didn't know that.

### The Problems

This item is out of stock at [Monoprice.com](https://www.monoprice.com/product?p_id=35877) and I'm not sure if they ever plan to restock. Monoprice seems to be discontinuing their line of Z-Wave products.

The smart plug can only fit in the bottom of the wall outlet and is so bulky that it blocks the top outlet as well. I couldn't connect the Monoprice plug and surge protector (with an angled connector). Using an AC extension cord with the plug added too much weight that the outlet could not support.

The USB ports are always-on and cannot be remotely turned off. It would have been an awesome feature to have, as I could cut off power to security cameras if I was at home, but alas.

### Installation and Smart Home Integration

The Monoprice plug pairs to SmartThings and Home Assistant like any Z-Wave device. It is treated as a generic Z-Wave plug. Energy usage is reported in SmartThings without the need for an additional device handler.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/monoprice-plug-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Easily pairs with Home Assistant as a generic Z-Wave plug.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Good</strong><br>No native integration, but works through SmartThings or Home Assistant.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/monoprice-plug-st.png" />
      <figcaption>
      <strong>SmartThings: Good</strong><br>Easily pairs as a generic Z-Wave plug. Also monitors energy usage.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/not_available.png" />
       <figcaption>
         <strong>Monoprice App: N/A</strong><br>A native app doesn't exist.</figcaption>
      </figure>
	</div>
</div>