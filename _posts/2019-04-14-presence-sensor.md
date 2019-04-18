---
layout: page
title: Presence Sensors
short_title: presence-sensor
excerpt: Everyone is carrying GPS trackers on their phones, so why not leverage it for home automation?
permalink: /presence-sensor
competitors: "SmartThings, iBeacons, Bluetooth LE devices, SmartThings, Life360, Tile, iCloud, nmap, so many more."
image: assets/images/overlay-ws/presence-sensor.jpg
image_credit: William Hook via Unsplash
image_url: https://unsplash.com/@williamtm
categories: 
    - "Sensor"
    - "Security"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\smartthings.png){:.image.logo} | ![](assets\images\logo\icloud.jpg){:.image.logo}  |   ![](assets\images\logo\nmap.jpg){:.image.logo}
|:-:|:-:|:-:
|  ![](assets\images\logo\life360.png){:.image.logo}   |![](assets\images\logo\tile.png){:.image.logo}   | 


## What you need to know

Presence detection is the ability to detect whether someone is in or out of a specified area, like home, at work, or school. Detection can be simple binary state (home/away) or complex (exact GPS coordinates) and usually relies on a mobile app or physical device—like a Tile tracker—to determine your location. I mainly use device trackers as another data point to enhance automations (e.g. if I arrive at home and open the door, then turn on the lights), and in a few scenarios, to unlock and lock doors. To me, a reliable device tracker is one that can detect I’m home right before I reach the door.

It took some time to find a capable presence sensor that was timely enough to update (within a minute’s notice), but it exists!

### Considerations before adding a presence sensor

<ul class="alt">
  <li><strong>When designing automations, make sure to test, test, and test.</strong> There are odd issues where for one millisecond, the sensor mistakenly reports you are home and opens the garage to intruders.</li>
  <li><strong>Make sure you have consent</strong> before installing a GPS tracking app like Tile or Life360.</li>
</ul>

### What you get with a presence sensor

<ul class="alt">
  <li> Design automations using geofencing like announcements (Dan is arriving home).</li>
  <li>Tell the difference between someone arriving at home and opening the door, versus opening the door. </li>
</ul>


### Recommended Reading

<ul class="alt">
  <li>Life360 works with <a href="http://workswith.life360.com/">SmartThings</a></li>
  <li>Home Assistant components for <a href="https://www.home-assistant.io/components/nmap_tracker/">nmap</a> and <a href="https://community.home-assistant.io/t/life360-device-tracker-platform/52406">Life360</a></li>
</ul>


<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
          <img src="assets\images\logo\nmap.jpg" alt=""/>
        <figcaption>
          A very creepy Nmap logo. <strong>|  Nmap</strong>
        </figcaption>
</figure>

## Nmap

Nmap is a network scanning tool that has many uses, though at a basic level it scans the network for connected devices. In Home Assistant, we repurpose the Nmap component as a device tracker: it scans the network for my phone (which is on the Wi-Fi network) and updates device status to ‘home’ if online, and ‘away’ if offline. **I like Nmap as it is a simple, non-intrusive service that doesn’t require installing an app, and doesn’t track location any further than the house.** That makes it easy to convince my roommates to use it as they don’t have to do anything on their phones, other than take their phones when they leave the house.

I have one goal with these device trackers, which is to update location status before I reach the door. This lets me unlock the door or open the garage door right as I arrive. In my testing, results have been very positive. Status changes happen in less than a minute. Nmap is fast enough to detect when I’m in the garage and about to head to the door. 

### The Problems

There are a few things you should know before using nmap. Tracking from away to home is deadly fast, but it takes longer to detect someone leaving home. This is a design choice that is reversible in settings in order to save battery life on the device.  Nmap is limited to tracking on the home Wi-Fi network, so you can’t track whether someone is at work or school.

Nmap’s accuracy is dependent on a strong Wi-Fi network that can reach just outside your garage or front door. Using a Wi-Fi mesh system or a powerful network router makes this a non-issue, but if you your phone doesn't connect to the Wi-Fi by the time you reach the front door or garage, then **nmap** won't work for you.

Nmap's accuracy also varies by phone, at least with the few Android phones I've tested. I~ On all phones I've tested, there were a few instances where~ switched to "not home" for one second. THat's why I would not create any automations that automatically unlock a door based on presence detection.

Some on the HA forums are having issues, where the nmap is kicking devices off the network. ANyone with aggressive battery saver ~ may find that nmap doesn't detect on the wifi network anymore. If you're not in the Wi-Fi network, then nmap won't detect it.

### Installation and Smart Home Integration

The **``Nmap``** component is available on Home Assistant only, but the configuration is incredibly easy to fill out. Once a configuration is added, a Home Assistant sensor will appear:

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets\images\integrations\nmap-ha.png" />
        <figcaption>
          <strong>Home Assistant: Great</strong><br>  A view of the nmap component in Home Assistant.
        </figcaption>
      </figure>
	</div>
</div>
<p></p>


<!-- Product Review section -->
<hr class="minor" />

## Life360

Life360 is probably the next best choice, though it is just a bit too slow at updating location to be used for something like unlocking the door. I've set larger geofences so detection could happen faster, but it still failed. I've sat in my car on the driveway, looking at my phone, waiting for an update. The update didn't happen until I opened the app.

Life360 can be used as a presence sensor in both SmartThings and Home Assistant, though there is more delay with SmartThings.

<!-- Product Review section -->
<hr class="minor" />

## The Competition

In my process of finding the right device tracker, I’ve tested a few other platforms and shared my thoughts. Unfortunately, ``nmap`` was the only one I could rely on.  At least you will know which ones to skip.

|             | Works in SmartThings | in Home Assistant | Time Accuracy      |                                                              |
| ----------- | -------------------- | ----------------- | ------------------ | ------------------------------------------------------------ |
| nmap        |                      | X                 | Less than a minute | **Good:** Fast status update, no interaction with household members needed. Additional app not required.<br>**Bad**: Only useful for detecting home/away status. Requires decent Wifi router. Can drain phone battery. |
| iCloud      |                      | X                 |                    | **Good:**<br>**Bad:** Current Home Assistant implementation requires re-authentication every two months if using two-factor auth. Requires saving iCloud password in text file. |
| iBeacons    |                      | X                 |                    |                                                              |
| Life360     | X                    | X                 | 1 to 2 minutes     | **Good**: Life360 In Home Assistant, there is only one-minute delay. Can set multiple geofences for home, work, school.<br>**Bad:** Life360 in SmartThings, I’ve experience a one-hour delay. Provides too much location details. Not good enough. |
| Tile        |                      | X                 | Terrible           | **Good:** None.<br>**Bad:** Completely inaccurate. Location update can take hours to days. Provides too much location details. |
| Nest        |                      | X                 | Terrible                | **Good:** None.<br>**Bad:** Requires installation of Nest app and enable ‘Home/Away Assist’ feature to work. Status update ranges from minutes to several hours delay. |
| SmartThings | X                    | X                 | Terrible           | **Good:** None.<br>**Bad:** It never detected when I was away. Location does not update **AT ALL** unless SmartThings app is opened on user’s phone, which is unlikely. |

