---
layout: page
title: Smart Remotes
short_title: smart_remotes
excerpt: A slightly smarter universal remote
update: "<strong>Nov 28, 2019:</strong> I reviewed the best (Logitech Harmony) and worst (Broadlink) smart remotes!"
competitors: "Logitech Harmony, Broadlink"
permalink: /smart_remote
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

It is unfortunate that a smart remote cannot compare against a real smart media device that can report its current state (on/off, input) to Home Assistant. A smart remote doesn't know if a TV is already powered on or what its current input is. That information is necessary for useful automations, though there are workarounds. The smart remote may just be a glorified universal remote, but it is still a useful an inexpensive way to add more control to your smart home.

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
  <li><strong>Identify which your devices use infrared (IR), radio frequency (RF), Wi-Fi or bluetooth remotes.</strong> This matters if you are deciding between buying a Broadlink RM Mini3 (IR only), RM Pro (RF & IR) or Logitech Harmony Companion (supports all of the above).</li>
  <li>While there are a slew of Logitech Harmony and Elite products, I think most people need only the <a href="https://amzn.to/2XuEk2h">Logitech Harmony Companion.</a></li>
  <li>Check the <a href="https://support.myharmony.com/en-us/compatibility">Logitech Harmony compatibility list</a> or one of many incomplete crowd-sourced remote code databases like <a href="https://github.com/probonopd/irdb">IRDB</a> for compatibility with your remote.</li>
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
  <img src="assets\images\product-photo\ecobee-thermostat.png" alt=""/>
  <figcaption>
    The Ecobee4. <strong>| Ecobee</strong>
  </figcaption>
</figure>

## Broadlink RM Mini3

**I shouldn't highlight the Broadlink RM Mini3 as the first review, but everyone needs to know that the [Broadlink RM Mini3](https://amzn.to/2pxbima) is simply not good.** It is the most difficult product to install because the mobile app (the primary method of installation) fails to connect to the Mini3 and complete setup. If a company can't get the setup process right, that doesn't bode well for the rest of the product. Granted, there haven't been any issues after setup, but the frustration I experienced to get to the Mini3 to a working state is something I refuse to go through again. The only positive for the RM Mini3 is the cheap price ($15 on eBay), which is why I only recommend the Mini3 to tech enthusiasts who like to test their patience with the crappiest of products. 

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

Stopping here gets you a functional universal remote app with limited voice control. To get the most out of the Mini3, we need to integrate with Home Assistant.

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
        <img src="assets/images/integrations/ecobee-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Requires an Ecobee developer account, then add the API key to the HA config. Has full functionality in HA.        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Great</strong><br>Officially supports Google Assistant. I rarely used it though!
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/ecobee-st.png" />
      <figcaption>
      <strong>SmartThings: Great</strong><br> Officially supports SmartThings, easy to set up.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/ecobee-app.png"  />
       <figcaption>
         <strong>Ecobee App: Great</strong><br> It's simple and easy to use.
       </figcaption>
      </figure>
	</div>
</div>


<!-- Product Review section -->
<hr class="minor" />
<figure class="align-left">
  <img src="assets\images\product-photo\nest-thermostat.png" alt=""/>
  <figcaption>
    The Nest 3rd Gen <strong>| Alphabet, Inc.</strong>
  </figcaption>
</figure>

## Nest Thermostats

**Nest thermostats were my original recommendation, but Google announced it is ending the Developers for Nest program by August 31, 2019, which will break SmartThings and Home Assistant integration.** Though I never used the integration in any meaningful way, it was still nice to have indoor temperature data reported in Home Assistant. With Google's current plans to close off its smart home ecosystem, I see no reason to continue recommending Nest when [Ecobee](#ecobee-thermostats) thermostats can do the same job. I just hope Ecobee doesn't follow the same path as Nest.

**If you're fine controlling the thermostat through the app or voice control, then I recommend any smart thermostat currently on sale, which is usually the Nest E. It has all important features of the [Nest 3rd Gen](https://amzn.to/2IC72re), but regularly goes on sale for $130 or less.** Get the Nest 3rd Gen for $180 if you want a nicer looking, metal finish on your thermostat. Ecobees are just as good as Nest, so there is no wrong choice here.

Honestly, there is not much to rave or complain about -- the Nest is what you expect out of a smart thermostat. The Nest app is straightforward to use, and according to [this security study](https://www.tomsguide.com/us/smart-home-leaky-apps,news-29319.html) of smart home apps, Nest is one of the few apps that encrypts communication between the thermostat and Nest app, even when on the same local network. 

### The Problems

Google ended the **Developers for Nest** program, meaning it is not possible (through conventional ways) to control the thermostat to a home automation platform like Home Assistant or SmartThings. A workaround exists for Home Assistant using the [Badnest](https://github.com/USA-RedDragon/badnest) custom component, but it uses an unadvertised web API that could be shut down in the future.

There aren't any major problems with Nest, but the **Home/Away Assist** feature can be very slow to detect changes in location. I've compared Nest times to actual times (tracked with Home Assistant) and have seen hour-long gaps in detection. I've also arrived home to see that the Nest cameras remained on (should be off when someone is home) and the thermostat not adjusted. If you want to come home to a warm house, the most reliable way is to use the Nest app before heading home.

### Installation and Smart Home Integration

Physical installation is not difficult, but you need to use the [Nest compatibility checker]("https://nest.com/works/) if your home’s existing wiring is compatible. I had to call tech support once because there were more wires in my existing installation than what was covered in the installation guide. Physical installation requires some basic do-it-yourself **DIY** skills like drilling holes and handling of electrical wires.

Nest thermostats come with a wall plate to cover the gaping hole left by the previous thermostat. How nice!

**Nest integrations with SmartThings and Home Assistant will break after August 31, 2019, due to the end of the Developers for Nest program.** A workaround exists for Home Assistant with the [Badnest](https://github.com/USA-RedDragon/badnest) custom component, but it uses an unadvertised web API that could be shut down in the future.

Very rarely do I need to change the temperature, so home automation integration is not all that important to me. I find that using the app is the most convenient way to fiddle with the thermostat. 



<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/nest-thermostat-ha.png" />
        <figcaption>
          <strong>Home Assistant: Bad</strong><br>It works now, but integration will stop working after August 31, 2019.
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
      <img src="assets/images/integrations/nest-thermostat-st.png" />
      <figcaption>
      <strong>SmartThings: Bad</strong><br> Works now, but integration will stop working after August 31, 2019.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/nest-thermostat-app.png"  />
       <figcaption>
         <strong>Nest App: Great</strong><br> Simple, easy-to-use.
       </figcaption>
      </figure>
	</div>
</div>
<p></p>
