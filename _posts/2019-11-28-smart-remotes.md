---
layout: page
title: Smart Remotes
short_title: smart-remotes
excerpt: A slightly smarter universal remote
update: "<strong>Nov 28, 2019:</strong> I reviewed the best (Logitech Harmony) and worst (Broadlink) smart remotes!"
competitors: "Logitech Harmony, Broadlink"
permalink: /smart-remotes
image: assets/images/overlay-ws/smart-remote.jpg
image_credit: Dan Nguyen
categories: 
    - "Gadgets"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\logitech-harmony.png){:.image.logo} |  ![](assets\images\logo\broadlink.png){:.image.logo} 
|:-:|:-:
| **Harmony hub** | **RM Mini 3**


## What you need to know

Devices like fans, air conditioners, and older media devices are operable only through physical buttons or remote. While somewhat elegant solutions exist to physical push buttons remotely (see [Switchbot](https://www.switch-bot.com/)), a better solution exists for remote-controlled devices: smart remotes. It functions like a universal remote hub but the addition of Wi-Fi allows for remote control of the hub and remotes using smartphone apps, voice control and Home Assistant, as well as the ability to access an online database of remote codes. The remote database is especially useful if you no longer have the original remote to learn commands from.

It is unfortunate that a smart remote cannot compare against a real smart media device that can report its current state (on/off, input) to Home Assistant. A smart remote doesn't know if a TV is already powered on or the current video input. That information is necessary for useful automations, though there are workarounds (explained later). The smart remote may be a glorified universal remote, but it is still a useful an inexpensive way to add more control to your smart home.

If you're thinking about what items can be controlled with a smart remote, here are some examples:

- Older TVs, sound bars, AV receivers
- Portable air conditioners and heaters
- Video projectors, motorized projector screens
- Karaoke machines
- Cable boxes, Blu-ray and DVD players
- Motorized blinds
- Motorized air vents

### Considerations Before Buying A Smart Remote

<ul class="alt">
  <li><strong>Identify which of your devices use infrared (IR), radio frequency (RF), Wi-Fi or bluetooth remotes.</strong> This matters if you are deciding between buying a Broadlink RM Mini3 (IR only), RM Pro (RF & IR) or Logitech Harmony Companion (supports all of the above).</li>
  <li>While there are a slew of Logitech Harmony and Elite products, I think most people need only the <a href="https://amzn.to/2XuEk2h">Logitech Harmony Companion to connect to Home Assistant.</a></li>
  <li>Check the <a href="https://support.myharmony.com/en-us/compatibility">Logitech Harmony compatibility list</a> or one of many incomplete crowd-sourced remote code databases, such as <a href="https://github.com/probonopd/irdb">IRDB</a>, for compatibility with your remote.</li>
</ul>


### What You Get With a Smart Remote

<ul class="alt">
  <li>A smarter universal remote that is controllable via smartphone, voice assistant, or Home Assistant dashboard.</li>
  <li>Automatically turn on the video projector and motorized projector screen when a media device is awakened.</li>
  <li>Control old media devices with a voice assistant.</li>
</ul>


### Recommended Reading

<ul class="alt">
  <li>Purchase the <a href="https://amzn.to/2XuEk2h">Logitech Harmony Companion</a> or <a href="https://amzn.to/2pxbima">Broadlink RM Mini3</a> from Amazon.</li>
  <li>Logitech Harmony review at the <a href="https://thewirecutter.com/reviews/the-best-universal-remote-control/">Wirecutter.</a></li>
  <li>Tools to set up Broadlink devices: Broadlink Bridge <a href="https://github.com/lbschenkel/hass-addon-broadlink-bridge/tree/master/broadlink-bridge">Hass.io add-on</a>, <a href="https://github.com/mjg59/python-broadlink">Broadlink Python library</a>, <a href="http://rm-bridge.fun2code.de/">RM Bridge</a></li>
</ul>

<!-- Product Review section -->
<hr class="minor" />
<figure class="align-left">
  <img src="assets\images\product-photo\broadlink-mini3.png" alt=""/>
  <figcaption>
    The Broadlink RM Mini3. <strong>| Broadlink</strong>
  </figcaption>
</figure>

## Broadlink RM Mini3

**I shouldn't highlight the Broadlink RM Mini3 as the first review, but everyone needs to know that the [Broadlink RM Mini3](https://amzn.to/2pxbima) is simply not good.** It is the most difficult product to install because the mobile app (the primary method of installation) fails to connect to the Mini3 and complete setup. If a company can't get the setup process right, that doesn't bode well for the rest of the product. Granted, I haven't had any issues after setup, but the frustration I experienced to get to the Mini3 to a working state is something I refuse to go through again. The only positive for the RM Mini3 is the cheap price ($15 on eBay), which is why I only recommend the Mini3 to tech enthusiasts who like to test their patience with the crappiest of products. 

Of all the cheap, Chinese branded smart remotes, Broadlink is the most supported platform. I see Home Assistant forum users in Europe and South America regularly talking about Broadlink integration. The company also sells the more expensive RM Pro+, which supports RF remotes (older TVs and set-top boxes use it), but I went for the IR-only RM Mini3 because all of my remotes are infrared. I don't recommend buying the RM Pro+ because for a few more dollars more, you are better off purchasing the superior Logitech Harmony hub. 

### The problems

The issues are numerous with this one that it needed to be in a list.

- **Painful installation process:** Connecting the Mini3 to a Wi-Fi network is difficult, whether using 2.4ghz (recommended) or a Wi-Fi mesh network (not recommended). If the initial setup through the app fails, you can set the Mini3 into AP mode where it broadcasts a Wi-Fi network to connect and set up (ala Chromecast), but I spent hours repeating the instructions until it finally connected. It is unbelievable that following setup instructions doesn't guarantee success and random luck is needed. If you are familiar with Python, using the [python-broadlink](https://github.com/mjg59/python-broadlink#example-use) library can set up without using the Broadlink iHC app.
- **Home Assistant integration is complicated:** The Broadlink [component](https://www.home-assistant.io/integrations/broadlink/) doesn't use the Home Assistant [remote](https://www.home-assistant.io/integrations/#remote) platform, but instead integrates a remote command as a switch. A switch make sense for some remote commands (on/off, volume up/down), but not commands like 'OK', 'Exit' or 'Menu'. Exporting the remote codes is a lengthy process that starts with using the Broadlink app to export the codes to a file, running a Python2 script to convert the file to BASE64 format, and adding `switch` entries to the `configuration.yaml` file. Or you can skip the Broadlink app by learning each remote code using the Home Assistant `broadlink.learn` service. Both methods are tedious and will likely take an hour or your time.
- **Weak IR emitters and no support for IR extenders:** My sound bar has a limited range to receive IR signals, so I needed to place the Mini3 directly on the sound bar for it to receive the signals reliably. Without an option for IR extenders, don't expect the IR signal to be very reliable unless the Mini3 is aiming directly at the device you're trying to control.
- **Bad out-of-the-box Google Home integration:** Google Home supports a number of device types (see [Available Domains](https://www.nabucasa.com/config/google_assistant/)), but the Broadlink integration doesn't make use of it correctly. Sound bars aren't supported and there are no workarounds using Broadlink's integration. However, if you use the Home Assistant integration and connect with Google Assistant, the Home Assistant switches (which are remote commands) can be seen in Google Assistant. 
- **The Broadlink iHC app asks for too many permissions:** the Broadlink iHC app asks access to: the camera, contacts, GPS location, microphone, file storage (to export codes), phone status and identity, and a shitload of other data. In comparison, the Logitech Harmony app asks for: location (network-based), microphone, and other, much more reasonable user data (network access, bluetooth). Both apps do the same thing, yet one is more pervasive for unexplained reasons. Use the python-broadlink library to connect the Mini3 to a WiFi network without using the Broadlink apps.

### Installation and Smart Home Integration

The RM Mini3 can be powered with any 1A USB charger and micro USB cable--my 4-port USB charger has no problem powering it. Connecting to the Wi-Fi network is done using the Broadlink Intelligent Home Center (iHC) app ([Android](https://play.google.com/store/apps/details?id=cn.com.broadlink.econtrol.plus) and [iOS](https://apps.apple.com/us/app/intelligent-home-center/id1084990073)), though this method didn't work for me. An alternate method involves setting the Mini3 into AP mode by holding the reset button on the device, connect to its broadcasted Wi-Fi network, and let iHC app configure the rest. Unfortunately, neither method works well, requiring repeated trial and error (and luck) to work. 

If you want to avoid using a Chinese app that is potentially taking your personal data, take the longer route by using the [pybroadlink](https://github.com/mjg59/python-broadlink#example-use) Python script to send your Wi-Fi network credentials.

After connecting the Mini3 to the Wi-Fi network, you can use the IHC app and search for your remotes in Broadlink's closed-source database, though finding a remote doesn't mean that all remote commands are included. Luckily, learning commands from a physical remote is easy with a few button presses on the app and remote.  

Stopping here gets you a functional universal remote app with limited voice control. But to get the most out of the Mini3, we need to integrate it with Home Assistant.

A [Broadlink component](https://www.home-assistant.io/integrations/broadlink/) for Home Assistant exists, but is one of the more difficult integrations to set up. You need the IP and MAC address of the Mini3--which can be found in your network router's settings or an Android app like [Fing](https://play.google.com/store/apps/details?id=com.overlook.android.fing). A typical configuration for a Broadlink switch in Home Assistant looks something like this:

```
- platform: broadlink
  host: 192.168.1.111
  mac: 'A1:B2:34:56:7C:8D'
  type: rm_mini
  switches:
    soundbar_power:
      friendly_name: "Soundbar Power"
      command_on: 'JgBQAAABH5MSExITExIRExITERQSEhITETgROBE4ETgROBE4EjcROBEUERMSExEUERMSExE4ERQSNxE4EjcSNhM2EzcSEhI3EgAFKQABJkkSAA0FAAAAAAAAAAA='
      command_off: 'JgBQAAABH5MSExITExIRExITERQSEhITETgROBE4ETgROBE4EjcROBEUERMSExEUERMSExE4ERQSNxE4EjcSNhM2EzcSEhI3EgAFKQABJkkSAA0FAAAAAAAAAAA='
```

After setup, there is no indication that Home Assistant successfully connected to the Mini3. You need to manually create switches for each remote command. 

There are several ways to get the remote commands into Home Assistant: learn commands in Home Assistant using the `broadlink.learn` service, use the new [Broadlink-bridge Hass.io add-on](https://github.com/lbschenkel/hass-addon-broadlink-bridge/tree/master/broadlink-bridge), or export commands from [e-Control app](https://play.google.com/store/apps/details?id=com.broadlink.rmt&hl=en_US) to your phone with the [Python2 script](https://community.home-assistant.io/t/broadlink-e-control-to-yaml/15548) from user @renetode. Instructions are listed in the [Broadlink documentation](https://www.home-assistant.io/integrations/broadlink/) for Home Assistant. Unfortunately, the remote codes come in multiple formats (hex, base64, Pronto Hex) so it is not easy to take remote codes from IRDB and use with the Mini3.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/broadlink-ha.png" />
        <figcaption>
          <strong>Home Assistant: Poor</strong><br>The existing component and add-on is difficult to configure. Every command is treated as a switch.</figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Average</strong><br>More functionality available using HA >> Google Assistant integration
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/not_available.png" />
      <figcaption>
      <strong>SmartThings: N/A</strong><br> Integration doesn't exist.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/broadlink-app.png"  />
       <figcaption>
         <strong>Broadlink iHC App: Poor</strong><br> Extremely difficult setup process. Works fine afterwards.
       </figcaption>
      </figure>
	</div>
</div>


<!-- Product Review section -->
<hr class="minor" />
<figure class="align-left">
  <img src="assets\images\product-photo\logitech-harmony.png" alt=""/>
  <figcaption>
    The Logitech Harmony Companion.<strong>| Logitech</strong>
  </figcaption>
</figure>

## Logitech Harmony

**If you need a smart remote in your setup, then I recommend the [Logitech Harmony Companion](https://amzn.to/2VqmcWs) and ONLY this model.** It includes a physical remote and the Harmony hub, which is all you need to connect to Home Assistant and gain much more functionality. I do not recommend the Harmony Ultimate, Elite, Express, or the Pro because you are paying for a remote with a fancy LCD screen and not much else. I recommend the Harmony because it is easy to set up and use with the mobile app, and the integration with Home Assistant is almost effortless. For a detailed review, see the [Wirecutters' recommendation](https://thewirecutter.com/reviews/the-best-universal-remote-control/) for the Logitech Harmony Companion.

Even though the Logitech Harmony hub is approaching five years of age (a lifetime in the tech gadget world), it continues to support a surprising number of modern devices, like the Apple TV, Fire TV, and Roku devices. Part of this support can be attributed to (paid) contractual agreements with those companies, but the decision to include bluetooth and Wi-Fi device control in the first generation of Harmony devices is the reason why the Harmony is still useful today. As a bonus, the hub features IR extenders to reach devices hidden behind media consoles or TV stands. Logitech has thought of every use case for media centers and has a solution ready.

If you need another reason why the Logitech Harmony hub is worth the extra $40, then look no further than the mobile app. Despite not explicitly supporting 5ghz and Wi-Fi mesh networks, I had no issues connecting the Harmony hub to my Google Wifi network. The mobile app is intuitive to use and Logitech's remote database is likely the most comprehensive, closed-source database in existence. I've searched the database and found remote codes that every media device I've used in the past five years.

### The Problems

On December 2018, Logitech removed support for the local XMPP API from the Harmony hub, which broke integration with Home Assistant and other home automation platforms. After some [deserved backlash](https://www.home-assistant.io/blog/2018/12/17/logitech-harmony-removes-local-api/), Logitech partially reversed their decision by offering a firmware that re-enables XMPP API and promised to continue supporting XMPP API for local control only. This event serves as a reminder that companies may attempt to take away control from customers if it interferes with their business objectives (like Nest and Google).

All smart remotes suffer from the inability to tell whether a device is already powered on. So unless you and your family commit to using only the Logitech remote, there will be issues where the Logitech physical remote is programmed for the wrong use. Think about it this way: if you turn on the Playstation 4 and TV using the controller and the Harmony was previously used to watch cable TV, then the Logitech physical remote is set to control the cable box, not the Playstation 4. This inconvenience can be fixed by running the Harmony activity again, but then makes the experience more manual than automated.

### Installation and Smart Home Integration

Connecting the Harmony hub to the Wi-Fi network is easily handled through the Harmony mobile app. I've connected the hub to Wi-Fi mesh networks without issue. Setting up remote control of media devices in the Harmony app is just as easy, with the upside that all registered devices and Harmony activities are transferable to Home Assistant.

The [Harmony component](https://www.home-assistant.io/integrations/harmony/) in Home Assistant takes less than 30 minutes to set up and start sending remote commands. All that is required in the configuration is the static IP address of the Harmony hub, like so:

```
remote:
  - platform: harmony
    name: Bedroom
    host: 10.168.1.13
```

Home Assistant connects to the Harmony hub and spits out an XML-formatted file (called harmony_hub_name.conf ) that lists every Harmony activity and command for every device configured on the hub. By using the Home Assistant remote.send_command or remote.turn_on service with the command or activity name listed in the .conf file, Home Assistant commands the Logitech Harmony hub to send a remote command to turn on the TV. I use button-card Lovelace card to create a clean-looking media center dashboard, where I can watch TV with the press of a button.

<figure class="align-center">
 <a class="image-link" href="assets\images\other\homeassistant-media02.jpg" ><img src="assets\images\other\homeassistant-media02.jpg" alt=""/></a>
 <figcaption>
My Home Assistant media dashboard, powered by Logitech Harmony. It's basically a fancy universal remote on a tablet.
 </figcaption>
</figure>

I mentioned there are workarounds for smart remotes to detect the state of media devices. For network-connected TVs that aren't supported by Home Assistant, I connect the TV to the Wi-Fi network, set a static IP address and use the Home Assistant [`ping`](https://www.home-assistant.io/integrations/ping/) sensor. State detection is accurate within 30 seconds, which is the scan interval I set. 

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/logitech-harmony-ha.png" />
        <figcaption>
          <strong>Home Assistant: Great</strong><br>Use a custom Lovelace Remote card to put a Harmony remote on your dashboard!
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Great</strong><br>Really easy to set up through Google Home. 
       </figcaption>
      </figure>
	</div>
</div>


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/logitech-harmony-st.png" />
      <figcaption>
      <strong>SmartThings: Okay</strong><br> Only Harmony activities are supported in ST.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/logitech-harmony-app.png"  />
       <figcaption>
         <strong>Harmony App: Great</strong><br> Intuitive to use, but fully customizable. Can add any button to the virtual remote screen.
       </figcaption>
      </figure>
	</div>
</div>
<p></p>
