---
layout: page
title: Home Automation Hub
short_title: home-automation-hub
excerpt: Though Google Home is slowly replacing its functions, a home automation hub is still necessary to perform real automations and local processing. 
permalink: /home-automation-hub
competitors: "Home Assistant, OpenHAB, Samsung Smartthings, Hubitat, Wink, Insteon Hub, Fibaro, Almond, Vera, Abode, and many more."
update: "<strong>April 16, 2019:</strong> Added my experience with Home Assistant Cloud."
image: assets/images/overlay-ws/home-automation-hub.jpg
image_credit: Dan Nguyen
categories: 
    - "Infrastructure"
    - "Home Automation"
---

<!--more-->
<!-- Overview Section -->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\smartthings.png){:.image.logo} |  ![](assets\images\logo\home-assistant.png){:.image.logo} 
|:-:|:-:
| **SmartThings v2** | **Home Assistant 0.90 (Hass.io version)** 

## What you need to know

I bet there is confusion about the need for a home automation hub, especially if you are already familiar with Google Home and the app. Yes, Google Home and the app can control the lights, outlets, and other devices, but you still have to use your voice or the app, and that gets tiring really quick. If you want to reach the point of true laziness — where the lights turn on before you even think about it — a hub is needed. To do more advanced routines like opening the garage automatically when arriving at home, a hub is the only way to do it, for now.

There are a few reasons why a home automation hub is still needed, for now. All your devices communicate through protocols—Zigbee, Z-Wave, Wi-Fi, RF, and Bluetooth LE are the most common standards. Also, some devices are fenced off from interacting with devices, but others have application programming interfaces (better known as APIs) to allow for intercommunication. A home automation hub has the hardware and software to send and receive those communications and interact with APIs and thus becomes like a command center. At a basic level, the hub performs the following:

<ol>
  <li>The hub gets periodic or real-time updates from the devices (“the TV just turned on”)</li>
  <li>The hub checks against its automations if certain conditions are met (“if the TV is on and it is after sunset…”)</li>
  <li>Then takes action and sends commands to the devices through device APIs or other means (“then turn on the TV lighting”).</li>
</ol>

The more devices you connect to the hub, the more control and data points it has for you to design smarter routines and automations. 

**Before going out to Best Buy and buying a home automation hub, there is nothing wrong with stopping here and becoming familiar with the smart devices you have.** I think it’s a good idea to hold off because the home automation hubs I’ve tested are still not stable enough and could use a few years of development.  In the meantime, look for a sale on Smartthings or Raspberry Pi hardware if you’re willing to go further. 

There are many home automation hubs to choose from that perform similar functions, but the implementation is very different for each. There is no way to know what hub is best for you unless you do the research and watch some demonstrations on Youtube. Even the Wirecutter, who previously recommended SmartThings, redacted their article about because they couldn’t agree on a recommendation. [Tom’s Guide](https://www.tomsguide.com/us/best-smart-home-hubs,review-3200.html) recommends SmartThings, but I don't think it is a thorough analysis that covers the negatives in detail. 

<!--Links Section -->
<hr class="minor" />

### Considerations Before Buying a Home Automation Hub

<ul class="alt">
  <li><b>Internet reliance.</b> SmartThings is heavily reliant on an Internet connection to function. If internet connectivity is spotty in your area, consider a hub that can operate locally, like <a href="https://www.home-assistant.io/">Home Assistant</a> or <a href="https://hubitat.com/">Hubitat</a>.</li>
  <li><b>Device compatibility with the big name IoT devices</b> like thermostats, security cameras, TVs, media centers, smart assistants. Some hubs have only a few, but tested integrations. The hubs that advertise 100+ integrations are likely unofficial that can break at any time (see <a href="https://www.theverge.com/circuitbreaker/2018/12/20/18150011/logitech-harmony-hub-remote-setup-security-update-broken-third-party-local-api">Logitech Harmony breaking XMPP integration</a>) or difficult to set up. </li>
  <li><b>Sensor Compatibility.</b> Buying a Z-Wave or Zigbee sensor doesn’t guarantee that it will work with your Z-Wave compatible hub.  SmartThings and Home Assistant have the highest compatibility, but it is still a good idea to research online before buying a sensor.</li>
  <li><b>Having a mobile app for the hub</b> is important for getting notifications and remote control of your connected devices. If you don’t mind having separate apps for thermostat, lighting, then this app is not as critical.</li>
  <li><b>Product Support.</b> Is the product still sold in stores or being actively developed by the community? If not, the hub likely won’t support any new integrations or security updates.</li>
</ul>

### What you get with a home automation hub

<ul class="alt">
  <li>True home automation! A smart home where things happen without having to use your voice or flip a switch. </li>
  <li>A way to control your lights and other connected devices remotely. You can setup a routine to turn on the lights at sunset, while on vacation.</li>
  <li>Notifications on home activity. When someone arrives and leaves, doors open, etc.</li>
  <li>A nice looking user interface (if you use Home Assistant).</li>
</ul>


### Recommended Reading


<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase a <a href="https://amzn.to/2IZoKqm">SmartThings hub</a>, <a href="https://amzn.to/2I2GbXc">Raspberry Pi 3B+</a>, <a href="https://amzn.to/2DH8G95">GoControl Z-Wave/Zigbee USB device (for Home Assistant)</a>, or <a href="https://amzn.to/2I4KyRI">Asus Tinkerboard S</a> from Amazon</li>
  <li><a href="https://graph-na04-useast2.api.smartthings.com/ide/apps">Developer portal</a> for SmartThings. This is where you add custom device handlers.</li>
  <li>Subreddits for <a href="https://www.reddit.com/r/homeassistant/">/homeassistant/</a> and <a href="https://www.reddit.com/r/SmartThings/">/smartThings/</a></li>
  <li><a href="https://wiki.webcore.co/">WebCoRE for SmartThings</a> lets users build complex automations. The tool is almost as easy as writing English, though it has some bugs.</li>
  <li>Get started with Home Assistant by trying out the <a href="https://demo.home-assistant.io/#/lovelace/0">live demo</a>, reading the <a href="https://www.home-assistant.io/getting-started/">instructions</a>, and reviewing <a href="https://github.com/dnguyen800/home-assistant-configuration-example">My Home Assistant configuration</a>. </li>
  <li>Integrate SmartThings with Home Assistant easily using the integration and <a href="https://www.nabucasa.com/">Home Assistant Cloud</a> ($5/month fee)</li>
  <li>Avoid the $5 fee by integrating SmartThings & Home Assistant using MQTT. An outdated tutorial was <a href="https://community.home-assistant.io/t/anyone-integrated-smartthings-into-hassio-yet/25324/7">written by yours truly</a>!</li>
</ul>

<!--Product Review Section -->
<hr class="major" />

<figure class="align-left">
 <img src="assets\images\logo\ha-st.png" alt=""/>
 <figcaption>
   An unholy matrimony. <b>|  Home Assistant/SmartThings</b>
 </figcaption>
</figure>

## Samsung SmartThings and Home Assistant

**Using [Samsung SmartThings](https://amzn.to/2IZoKqm) and Home Assistant together provides the functionality I need to do a proper media-focused smart home, but I hope to remove SmartThings eventually.** I first started off using SmartThings, then tried Home Assistant, and eventually decided to use both hubs together to leverage their strengths and mitigate weaknesses. 

In my solution, __SmartThings__ is the reliable one __(I know, debatable)__ that handles communications between most devices and performs basic light automations. I can pair door and motion sensors, the Philips Hue hub, MyQ garage door opener, Ecobee thermostat and Google Assistant to SmartThings easily enough. 

One of the major selling points for me (and a problem for others) with SmartThings is that most features can work remotely out of the box--I get notifications on my phone when something is happening in the house and can remotely control the lights while away. Home Assistant and Hubitat can't do this so easily as SmartThings, though I expect new developments in 2019 from Home Assistant Cloud in the future.

<figure class="align-center">
 <a class="image-link" href="assets\images\other\smartthings-app.jpg" ><img src="assets\images\other\smartthings-app.jpg" alt=""/></a>
 <figcaption>
The SmartThings Classic UI in tablet mode.
 </figcaption>
</figure>

The UI on the SmartThings Classic app is basic, but it works. You can create the most basic of basic automations through the app, but at least those will always work. There is a new SmartThings app (with a nicer UI) available, but I was unable to get most of my connected devices working with it.

### SmartThings' Problems

But that’s about all that SmartThings can do well. There is no product roadmap nor any interesting product developments or integrations in the past year, besides releasing a cheaper, slightly less functional hub. New official product integrations are non-existent. SmartThings would be a terrible product today if it weren't for the SmartThings community creating workarounds to make up for SmartThings' shortcomings. Several members created a new automation engine--[WebCoRE](https://www.webcore.co/)--which adds the ability to create advanced automations with conditional statements but relies on an internet connection to work.

I've also noticed that SmartThings notifications can be delayed when using the latest Android OS—as much as 15 minutes! There is no way I can use SmartThings as a security system with these delays. I’m only keeping the hub around until I get Home Assistant running stable.

<figure class="align-center">
 <a class="image-link" href="assets\images\other\homeassistant-02.jpg" ><img src="assets\images\other\homeassistant-02.jpg" alt="" /></a>
 <figcaption>
The Home Assistant web interface. It tooks months of learning to get it to this state.
 </figcaption>
</figure>

### SmartThings Installation

I can't get into the details of installing SmartThings, but there are a ton of online resources to help you. Here are some basic tips you should know:

- There are two SmartThings mobile apps: SmartThings Classic and SmartThings. The new SmartThings app is required to set up the Wi-Fi settings on the new SmartThings v3 hub. After setup, you can switch to SmartThings Classic, which is a more reliable app.
- Before adding a device to SmartThings, see if there is a custom device handler (search for "smartthings device handler" and the model number) you can install.
- Adding a Z-Wave or Zigbee device in SmartThings means putting the device in inclusion mode (usually pressing a physical button on the device multiple times), then pressing the **+** button in the SmartThings app to pair. See this [tutorial](https://www.androidcentral.com/how-add-new-smart-devices-your-smartthings-hub) for images. You should bring the device as close as possible (around 10ft) to the SmartThings hub when pairing.
- Get familiar with the [SmartThings IDE](https://graph.api.smartthings.com/) to install custom SmartApps, device handlers, and troubleshoot issues.

__Speaking of Home Assistant, it is an amazing, unstable platform that I use for its slick UI, hundreds of integrations, and advanced media automations.__ It is open source and can be run on cheap hardware like a [Raspberry Pi 3B+](https://amzn.to/2YRzixh), but nothing slower than that. Though not every integration is easy to set up, Home Assistant works with the latest and greatest products--from TVs and AV receivers to robot vacuums, lights, and homemade hardware. Without Home Assistant, I would have given up on home automation altogether, after being disappointed by SmartThings’ inability to do anything I would consider “smart.”

I could continue to explain why Home Assistant is great, but it's easier to try out the [demo](https://demo.home-assistant.io/#/lovelace/0) yourself. Or watch this video I made:

<div class="container">
   {%- include extensions/youtube.html id='v1c393EJ5ww' -%}
</div>
<p></p>

Home Assistant is necessary to do media automations that can show off the home theater. In my setup, Home Assistant acts like a universal remote, but much smarter — it knows what devices are powered on and what they’re currently doing.  Google Assistant integration with Home Assistant also allows provides much better voice control over media devices. I have several examples of how Home Assistant has automated a few things in my home:


- Home Assistant can broadcast a message on Chromecast Built-In speakers if someone is arriving home, a door is unlocked, or whatever you can think of.
- Chromecast Audio cannot turn on an AV receiver on its own, but Home Assistant can detect when the Audio is playing music and turn on the receiver automatically. 
- The Xbox One cannot turn on the TV on its own but using Home Assistant, I can detect when the Xbox One is on, and turn on the TV accordingly.
- The dashboard can shows music currently playing on Spotify, Plex, or any Chromecast speaker, along with media controls and cover art.


<figure class="align-center">
 <a class="image-link" href="assets\images\other\homeassistant-media.jpg" ><img src="assets\images\other\homeassistant-media.jpg" alt="" /></a>
 <figcaption>
A media-focused Home Assistant dashboard I created.
 </figcaption>
</figure>

If you're still curious about Home Assistant, start off by purchasing a <a href="https://amzn.to/2YRzixh">Raspberry Pi 3B+</a> or <a href="https://amzn.to/2I4KyRI">Asus Tinkerboard S</a>, a high-endurance SD card (for rPi only) and install Hass.io (a more restricted version of Home Assistant) by following this [guide](https://www.home-assistant.io/getting-started/). If you're an IT guru and have an existing server and Docker platform ready, then you can install Home Assistant or Hass.io as a service or Docker container.

I've shared my [Home Assistant configuration](https://github.com/dnguyen800/home-assistant-configuration-example) on Github as a learning example for beginners, though it's already become outdated after only a few weeks. Still, I explain how every Lovelace card and component is used.

### Home Assistant's Problems

Home Assistant is an amazing piece of software, but it is absolutely not for tech novices. The learning curve is high and the limited documentation is difficult for newcomers to grasp. Setting up the UI is difficult at first if editing YAML files directly, though the team is working on improving the UI editor.

When Home Assistant crashes (and it will), a technical person needs to be present to fix it. The instability is one of the reasons I keep SmartThings around so at least the lighting will continue to work if Home Assistant is down. I say give Home Assistant another year of development and it will be even more user-friendly to use.

### Connecting SmartThings and Home Assistant together

To get the best of both worlds, SmartThings and Home Assistant need to communicate with each other. Integrating SmartThings and Home Assistant is a difficult exercise, but it can be made easy, for a small price. The introduction of [Home Assistant Cloud](https://www.nabucasa.com/) and a new [integration](https://www.home-assistant.io/components/smartthings) have simplified the process so much that I just tried it and it took five minutes to integrate. I am in awe with how far Home Assistant has come along and offered functionality like this. It's quite amazing.

<p class="box">
<i>As of Home Assistant 0.90, it is possible to use the <a href="https://www.nabucasa.com/">Home Assistant Cloud</a> and the newly developed <a href="https://www.home-assistant.io/components/smartthings/">SmartThings integration</a> to easily connect SmartThings and Home Assistant together. Home Assistant Cloud is not free ($5/month), and I'm sure there are bugs to fix, but it's a good start.</i>
</p>

To integrate SmartThings and Home Assistant without HA Cloud, I previously used **``MQTT``**, a lightweight messaging protocol that translates messages between the two platforms. Once it is set up, any devices in SmartThings appear as native Home Assistant entities. I wrote a [tutorial](https://community.home-assistant.io/t/anyone-integrated-smartthings-into-hassio-yet/25324/7) for an older version of Home Assistant, but it’s still usable as of version 0.91. It is quite a difficult install and only recommend if you really want to learn how MQTT integration works.


#### Notifications from Home Assistant

The notification platform in Home Assistant is very basic and tedious to set up. Every single notification needs to be manually written as an automation. If you're good at writing automation templates, then the workload is reduced, but right now, it's a mess and I don't recommend investing much time in creating notifications. Getting notifications on your phone is much easier in 2019, thanks to a few new apps.

iOS phones can receive notifications after setting up the [iOS component](https://www.home-assistant.io/docs/ecosystem/ios/) and installing the Home Assistant [iOS app](https://itunes.apple.com/us/app/home-assistant-open-source-home-automation/id1099568401?mt=8). If your Home Assistant instance isn't exposed on the internet, you can still receive notifications through iCloud, but cannot respond back.


For Android phones with Google Play installed, I found that the easiest method to get notifications is using Home Assistant Cloud and the remote UI feature, and the [Ariela Android app](https://community.home-assistant.io/t/ariela-home-assistant-android-client-updates-thread), and the custom component [Ariela Notify](https://github.com/mCrissDev/HANotify). In the future, the official Home Assistant Android app will make the notification process simpler, but this is the easiest way I've discovered, for now.

<!--Product Review Section -->
<hr class="minor" />
## The Competition

![Hubitat logo](assets\images\logo\hubitat.png){:.image.dan-left}

### Hubitat 

I’ve been looking into a new SmartThings competitor called **[Hubitat](https://amzn.to/2XWjOqy)**. In-depth reviews aren’t common for Hubitat, but I gather it is a better version of SmartThings, but missing a few things like a proper mobile app and support for some cloud-dependent devices like the Lutron Caseta bridge. I decided against ordering Hubitat as it didn’t support the standard Lutron Caseta bridge, which I currently use at my house. There also aren't any Hass.io add-ons or integrations to connect with Home Assistant so I wouldn't be able to use it with my Hass.io instance.




