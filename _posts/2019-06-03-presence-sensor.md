---
layout: page
title: Presence Sensors
short_title: presence-sensor
excerpt: Everyone is carrying GPS trackers on their phones, so why not leverage it for home automation? Enter presence sensors.
update: <strong>June 3, 2019:</strong> Added a new software-based device tracker, Owntracks.
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
|  ![](assets\images\logo\life360.png){:.image.logo}   |![](assets\images\logo\tile.png){:.image.logo}   | ![](assets\images\logo\owntracks.png){:.image.logo} 


## What you need to know

Presence detection is the ability to detect whether someone is in or out of a specified area, like home, at work, or school. Presence can be represented as a binary state (home/away) or  as GPS coordinates and usually relies on a mobile app or physical device—like a Tile tracker—to determine your location. I mainly use device trackers as another data point to enhance automations (e.g. if I arrive at home and open the door, then turn on the lights), and in a few scenarios, to unlock and lock doors. To me, a reliable device tracker is one that can detect when I am arriving home, unlock the door right before I reach the door.

I haven't found the perfect presence sensor--yet. I want a non-intrusive ~.

### Considerations before adding a presence sensor

<ul class="alt">
  <li><strong>When designing automations, make sure to test, test, and test.</strong> There are odd issues where for one second, the presence sensor mistakenly reports you are home and opens the garage to intruders. Don't design an automation that does this.</li>
  <li><strong>Make sure you have consent</strong> before installing a GPS tracking app like Tile or Life360 on a person's phone.</li>
</ul>

### What you get with a presence sensor

<ul class="alt">
  <li> Design automations using geofencing, like opening the door when arriving home, arming the security system when away, or playing announcements on the speakers ("Dan is arriving home").</li>
  <li>Tell the difference between someone arriving at home and opening the door, versus opening the door. </li>
</ul>


### Recommended Reading

<ul class="alt">
  <li>Life360 works with <a href="http://workswith.life360.com/">SmartThings</a> and <a href="https://community.home-assistant.io/t/life360-device-tracker-platform/52406">Home Assistant</a></li>
  <li>Home Assistant components for <a href="https://www.home-assistant.io/components/nmap_tracker/">nmap</a> and <a href="https://www.home-assistant.io/components/owntracks/">Owntracks</a></li>
  <li>Use Owntracks with Home Assistant Cloud <a href="https://www.nabucasa.com/config/webhooks/">webhook support</a> to securely send your phone's location data to your Home Assistant instance. </li>
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

[Nmap](https://www.home-assistant.io/components/nmap_tracker/) is a network scanning tool that has many uses, though at a basic level it scans the network for connected devices. In Home Assistant, we repurpose the Nmap component as a device tracker: it scans the network for my phone (which is on the Wi-Fi network) and updates device status to ‘home’ if online, and ‘away’ if offline. **I like Nmap as it is a simple, non-intrusive service that doesn’t require installing a mobile app on each person's phone, and doesn’t track location any further than the house.** That makes it easy to convince my roommates to use it as they don’t have to do anything on their phones, other than taking their phones when they leave the house.

I have one goal with these device trackers, which is to update location status before arriving home and reaching the front door. Having this feature lets me unlock the door or open the garage door right as I arrive at home. In my testing with Nmap, the results have been very positive. Status changes happen in less than a minute and Nmap is fast enough to detect when I parked in the garage and about to head to the door. It is not good at detecting when someone leaves the house, which I will explain further in detail.

### The Problems

There are a few things you should know before using nmap. Tracking from **away to home** is wickedly fast, but it takes longer to detect someone leaving home. This is a design flaw that can be corrected by changing the scan interval, but will lead to more complications like decreased battery life on the user's phone, potential Wi-Fi disconnections, or accidentally marking a user as *away* when they are still at *home*. 

Nmap's accuracy also varies by smartphone--on the phones I tested, there were a few instances where the Nmap tracker incorrectly switched to **``not home``** for one minute and switched back. This issue was most prevalent on iPhones. The issue repeated so often that I needed to increase the **``home interval``** which is the number of minutes Nmap will not scan this device, assuming it is home, in order to preserve the device battery. With these types of issues, I would not create any automations that automatically unlock a door based on presence detection.

Nmap is limited to tracking on the home Wi-Fi network, so you can’t track whether someone is at work or school. Nmap’s accuracy is dependent on a strong Wi-Fi network that can reach just outside your garage or front door. Using a Wi-Fi mesh system or a powerful network router makes this a non-issue, but if you your phone doesn't connect to the Wi-Fi by the time you reach the front door or garage, then **nmap** won't work for you.

### Installation and Smart Home Integration

The **``Nmap``** component is available on Home Assistant only, but the configuration is incredibly easy to fill out in Home Assistant. The hardest part (which is still easy) is setting up a static IP address for the smartphone that will be tracked. This is done in the network router's settings and may require the phone's MAC address or local network IP address. Every router's setting is different, so use Google search for guidance.

To find the IP address of your phone, first make sure it is connected to your local wireless network. On iPhone, you go to the WiFi settings, select the network you are currently connected to, and you should see the IP address like so. On Android, the process is similar, except you need to expand the "Advanced" tab after selecting the wireless network. Or you can follow this [guide](https://www.makeuseof.com/tag/find-ip-address-mobile-smartphone/).


<div class="row">
	<!-- Break -->
	<div class="4u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/other/apple_ip_address.png" />
        <figcaption>
          IP address on iPhone. <strong>| Appuals</strong>
        </figcaption>
      </figure>
	</div>
	<div class="4u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/other/android_ip_address.png" />
       <figcaption>
         IP address on Android phones. <strong>| Makeuseof </strong>
       </figcaption>
      </figure>
	</div>
  <div class="4u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets\images\integrations\nmap-ha.png" />
       <figcaption>
         <strong>Home Assistant: Great</strong><br> Once the configuration is added, a Home Assistant sensor will appear like so.
       </figcaption>
      </figure>
	</div>
</div>
<p></p>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
          <img src="assets\images\logo\owntracks.png" alt=""/>
        <figcaption>
          <strong>|  Owntracks</strong>
        </figcaption>
</figure>

## Owntracks

Owntracks is a software-based device tracker application that is often recommended by Home Assistant users, and is now incredibly easy to set up with Home Assistant Cloud using the Webhooks ability. iOS and Android apps exist and work on the latest OS versions. The best part about Owntracks is that you choose where to send the location data--to a private MQTT or HTTP server--and no one sees the data except you. **For the most accurate and timely tracking, use Owntracks if you have consent.** Otherwise, use Nmap.

Initially, I didn't use Owntracks because it required my Home Assistant instance to be exposed on the internet. But now with Home Assistant Cloud [Webhooks capability](https://www.nabucasa.com/config/webhooks/), the setup is much easier, taking only minutes to install. I now recommend using Owntracks if users are okay with sharing location data from their phones, otherwise I default to Nmap.

### The Problems

The Owntracks app needs to be installed on the user's phone to use GPS data for tracking. While Owntracks was designed with [data privacy in mind](https://owntracks.org/booklet/features/security/), not everyone is willing to risk sharing that data. 

Balancing your phone's battery life and accurate location updates is difficult, but Owntracks offers various modes to suit each user's needs. I'm still testing Owntracks' various monitoring modes as described in the Owntracks [booklet](https://owntracks.org/booklet/features/location/), but Significant Location Change mode seems to work best for me.

### Installation and Smart Home Integration
Installing Owntracks on your phone is easy--search for the Owntracks app on [Google Play](https://play.google.com/store/apps/details?id=org.owntracks.android) or the [Apple App Store](https://itunes.apple.com/us/app/owntracks/id692424691?mt=8). Follow the instructions on the Nabu Casa [website](https://www.nabucasa.com/config/webhooks/) and also watch the embedded Youtube video--it is short and to the point.

You can enable Owntracks in the *__Home Assistant >> Configuration >> Integrations__* section. Once added, go to the *__Home Assistant >> Configuration >> Home Assistant Cloud >> Webhooks__* section to find the newly added Owntracks webhook, and enable by pressing the button. Copy the Public URL that is listed for the webhook into the Owntracks configuration (under Private HTTP, Host) and that is pretty much it. Assign a name and device ID that will be shown in Home Assistant.

<!-- Product Review section -->
<hr class="minor" />

## Life360

[Life360](https://www.life360.com/) is a location tracking platform tailored to families that easily integrates with SmartThings and Home Assistant and is probably the next best choice to Nmap and Owntracks, though location updates aren't fast enough for automations that unlock the door. I don't know how/where Life360 stores my location data, so I'd rather not share the data to third parties if possible. 



### The Problems

In an effort to improvoe the home/away detection with Life360, I've set larger geofences in the Life360 app and even sat in my car on the driveway, looking at my phone, waiting for an update, but the location updates were still too slow. Sometimes the location update didn't happen until I opened the Life360 app. Maybe you will have better luck than me, but I moved on to Nmap and Owntracks, which have been more reliable so far.

<!-- Product Review section -->
<hr class="minor" />

## The Competition

In my process of finding the right device tracker, I’ve tested a few other platforms and shared my thoughts. Unfortunately, **``nmap``** was the only one I could rely on.  At least you will know which ones to skip.

| Platform | Works in SmartThings | in Home Assistant | Time Accuracy      | Comments                                                             |
| ----------- | -------------------- | ----------------- | ------------------ | ------------------------------------------------------------ |
| nmap        |                      | X                 | Less than a minute | **Good:** Fast status update, no interaction with household members needed. Additional app not required.<br>**Bad**: Only useful for detecting home/away status. Requires decent Wifi router. Can drain phone battery. |
| iCloud      |                      | X                 |                    | **Good:** TBD<br>**Bad:** Current Home Assistant implementation requires re-authentication every two months if using two-factor auth. Requires saving iCloud password in text file. |
| iBeacons    |                      | X                 |                    |                                                              |
| Life360     | X                    | X                 | 1 to 2 minutes     | **Good**: Life360 In Home Assistant, there is only one-minute delay. Can set multiple geofences for home, work, school.<br>**Bad:** Life360 in SmartThings, I’ve experience a one-hour delay. Provides too much location details. Not good enough. |
| Tile        |                      | X                 | Terrible           | **Good:** None.<br>**Bad:** Completely inaccurate. Location update can take hours to days. Provides too much location details. |
| Nest        |                      | X                 | Terrible                | **Good:** None.<br>**Bad:** Requires installation of Nest app and enable ‘Home/Away Assist’ feature to work. Status update ranges from minutes to several hours delay. |
| SmartThings | X                    | X                 | Terrible           | **Good:** None.<br>**Bad:** It never detected when I was away. Location does not update **AT ALL** unless SmartThings app is opened on user’s phone, which is unlikely. |

