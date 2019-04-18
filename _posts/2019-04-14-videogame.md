---
layout: page
title: Video Game Consoles
short_title: videogame
excerpt: Video games come first, but consoles also offer many streaming media services, as well as Blu-ray playback.
competitors: "Microsoft, Sony, Nintendo"
permalink: /videogame
image: assets/images/overlay-ws/videogame.jpg
image_credit:  Fabian Albert on Unsplash
image_url: https://unsplash.com/@serumfabian
categories: 
    - "Media"
    - "Home Theater"
    - "Home Automation"
---

<!--more-->

#### I've personally tested the following:

|---
| ![](assets\images\logo\xboxone.png){:.image.logo} |  ![](assets\images\logo\sony-ps4.png){:.image.logo} | ![](assets\images\logo\nintendo.png){:.image.logo} 
|:-:|:-:|:-:
| **Xbox One X** | **Playstation 4 Pro** | **Nintendo Switch (2017)** 


## What you need to know

Video game consoles have always been a part of my media center, so it would be a glaring omission if I couldn’t include them in my smart home automations. Besides playing video games, I use them as blu-ray players for those rare occasions when I revisit a favorite movie, or watch something that's not on Netflix. The Xbox One makes for a noteworthy media streaming device—even segregated apps like Youtube TV, Amazon Video are available. If I had to choose only one device connected to my TV, it would likely be a videogame console because it plays games, blu-rays, and most major apps.

Consoles aren’t known to be open platforms, but several clever people developed ways to connect the Xbox One and Playstation 4 consoles to Home Assistant. These are unofficial methods that Sony or Microsoft could discontinue in the future, but I’ll give it a couple of years before that happens.

With Home Assistant integrations, I can see the game currently playing *(see examples below)*. It's not exactly useful, but it sure looks cool on the Home Assistant dashboard! The other benefit to integrating is that my TV lighting automations will be even more precise, now that I can detect if a game is playing.

### Considerations before buying a video game console

<ul class="alt">
  <li><strong>Only the Xbox One S and X support 4K Blu-ray.</strong> Playstation 4 Pro can play regular Blu-rays only.</li>
  <li><strong>If you use it as a media streaming device, you should purchase a media remote or use a Logitech Harmony remote.</strong></li>
  <li><strong>Consoles are slightly less convenient than media streaming devices to watch videos. It takes longer to boot up and start watching.</strong> You also lose a few features like voice control and casting. </li>
</ul>

### What you get with integrating a video game console

<ul class="alt">
  <li>Create more accurate lighting automations (e.g. turn on the lights when a game is playing).</li>
  <li>Use as a blu-ray player (XboxOne S & X supports 4K).</li>
  <li>Supports video and music apps like Hulu, Spotify, Netflix.</li>
  <li>Integration looks cool on Home Assistant.</li>
</ul>

### Recommended Reading
<ul class="alt">
  <li>Use Alexa on XboxOne support <a href="https://support.xbox.com/en-US/xbox-one/voice-and-digital-assistants/set-up-alexa-as-digital-assistant-xbox-one">article</a></li>
  <li>Home Assistant component for  <a href="https://www.home-assistant.io/components/ps4/">Playstation 4</a></li>
  <li>Tutorial for old Playstation4 <a href="https://community.home-assistant.io/t/playstation-4-ps4-custom-component/16974/207?u=dwinnn">integration</a> with Home Assistant</li>
  <li>Xbox One Hass.io <a href="https://github.com/hunterjm/hassio-addons">add-on</a></li>
</ul>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\xboxone.png" alt=""/>
 <figcaption>
The latest in the Xbox family: Xbox One X <strong>|  Microsoft</strong>
 </figcaption>
</figure>

## Microsoft Xbox One

When the Xbox One launched in 2013, it was supposed to be the ultimate media center where you could play games and watch TV—all on the same screen! Well, that idea failed horribly due to poor management decisions but the Xbox One gained some awesome features recently, like a 4K bluray player and plenty of supported video apps (Youtube TV, Hulu, Spotify). Smart home integration was recently added in the form of a Home Assistant (Hass.io) add-on and it’s quite impressive, with the ability to display the game currently playing in Home Assistant—all without any manual intervention. 

### The Problems

I’ve run into a few issues, like having to re-authenticate my Xbox account from time to time. It’s not a completely hands-off integration, but it’s not a critical component that I can survive without it working. 

### Installation and Smart Home Integration

The initial setup on Home Assistant is only difficult if you don’t read the instructions.  Install the Hass.io addon and authenticate to **``Xbox Live``** per the add-on instructions. Find your Xbox One’s device ID (see instructions again), then add the Xbox One media player platform and device ID in your configuration.yaml file. Be sure to read the instructions thoroughly!

Status updates to Home Assistant are quick—within one to two seconds—so lighting automations are responsive when I start playing a game. Videogame cover art appears automatically when a game is playing, which is a nice touch to the UI..

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/xboxone-ha.gif" />
        <figcaption>
          <strong>Home Assistant: Difficult</strong><br>Can be hard to install. Displays game cover art.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/amazon-echo.jpg" />
       <figcaption>
         <strong>Voice: Great</strong><br>Alexa works,  Google Assistant is coming.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/na.png"  />
      <figcaption>
        <strong>SmartThings: N/A</strong><br>Integration does not exist.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/xboxone-app.png" />
       <figcaption>
         <strong>Xbox App: Average</strong><br>Basic controls, no context.
       </figcaption>
      </figure>
	</div>
</div>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\playstation4.png" alt=""/>
 <figcaption>
The Playstation 4 is almost six years old! <strong>|  Sony</strong>
 </figcaption>
</figure>

## Sony Playstation 4

**As of Home Assistant 0.89, the Playstation 4 is supported with the same features as the Xbox One add-on.** It is even easier to authenticate using the new Home Assistant integration process, which makes this an easy recommendation if you already have a PS4. Most of the popular streaming video apps are available on PS4--even Plex! Remotely powering on the PS4 now works, so you can now use voice control for that. I’m happy that more people can use this integration and show off the game playing, and design lighting automations based on the PS4’s state.

### Installation and Smart Home Integration

I haven’t had any authentication issues with the Playstation 4 add-on like I did with the Xbox One. With the new component added to **Home Assistant 0.89**, installation is a breeze compared to the old method. For reference, here is the <a href="https://community.home-assistant.io/t/playstation-4-ps4-custom-component/16974/207?u=dwinnn">tutorial</a> from Home Assistant user @cheynespc for directions to install the old Playstation 4 Hass.io add-on.

Video game cover art works on some but not all games. 

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/playstation4-ha.gif" />
        <figcaption>
          <strong>Home Assistant: Difficult</strong><br>Easier to install than before, though requires using PS4 mobile app.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
         <figcaption>
           <strong>Voice: Average</strong><br> Works through PS4>>HA>>Google Assistant. Basic commands work.
         </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/na.png"  />
      <figcaption>
        <strong>SmartThings: N/A</strong><br>Integration does not exist.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/playstation4-app.png" />
       <figcaption>
         <strong>Playstation App: Average</strong><br>Basic controls, no context.
       </figcaption>
      </figure>
	</div>
</div>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\nintendo-switch.jpg" alt=""/>
 <figcaption>
   The first generation Switch.<strong>|  Nintendo</strong>
 </figcaption>
</figure>

## Nintendo Switch

**No integration exists for the Nintendo Switch and it’s not likely to happen in the future.** If you need a method to detect if the Switch is connected to the dock, I would connect a LAN adapter to the the Switch dock and Home Assistant’s [**``nmap device tracker``**](https://www.home-assistant.io/components/nmap_tracker/) to detect the LAN adapter’s presence. Or, if the Switch uses a dedicated HDMI port and your TV and/or AV receiver is connected to Home Assistant, then create an automation that detects if that HDMI port is currently selected. I think the LAN adapter is the best method for detection though.