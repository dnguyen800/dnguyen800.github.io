---
layout: page
title: Security Systems
short_title: security-system
excerpt: A new era of affordable security systems is coming, thanks to companies like Ring, Simplisafe and Abode.
competitors: "Ring Alarm, Nest Secure, Simplisafe, Abode, alarm.com, Frontpoint Security, ADT"
permalink: /security-system
image: assets/images/overlay-ws/security-system.jpg
image_credit: Simplisafe
image_url: https://www.simplisafe.com
categories: 
    - "Security"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\simplisafe.png){:.image.logo} |  ![](assets\images\logo\smartthings.png){:.image.logo} 
|:-:|:-:
| **Simplisafe (latest version)** | **SmartThings (DIY Solution)** 


## What you need to know

Like the cord-cutting revolution with cable TV, the home security system market is entering a new era of affordable security monitoring without contracts. Professional installation isn’t needed with these systems unless you are looking to install wired sensors in the house.

Your security system purchase has an impact on home automation, as there are ways to use the security system’s sensors with your home automation platform to avoid duplicate sensors.  Abode and Ring offer unofficial integrations with Home Assistant, though your home automation platform may not be the most stable with this setup. So choose wisely!

There are few differentiating features between competitors as all professional security systems have the essential features: a 24-hour battery backup, cellular connection (included with monitoring service), and the “smashsafe” feature (if someone smashes a keypad or hub, you’re alerted).  These features are not available with DIY solutions without a clever homemade solution.

I’ve believe there are three categories I cover that will fit most people’s needs around security. If you are just a little bit serious about protecting your home, then I strongly suggest avoid the DIY route and look into an official provider like Ring.

### Considerations before buying a security system

<ul class="alt">
  <li>Decide on whether to build a DIY security system or purchase a professional one.</li>
  <li>Decide if you want to use home security sensors as part of your home automation platform, which may be more unreliable than separate sensors.</li>
</ul>


### What you get with a security system

<ul class="alt">
  <li>In theory, you get more reliable sensors that have been thoroughly tested with the security system.</li>
  <li>24/7 security monitoring at a low cost, around $10-25 a month.</li>
</ul>


### Recommended Reading

<ul class="alt">
  <li>The Wirecutter’s recommendation for <a href="https://thewirecutter.com/reviews/the-best-home-security-system/">home security system</a></li>
  <li>Article about recent <a href="https://gizmodo.com/amazons-ring-security-cameras-may-have-let-employees-sp-1831658669">internal security breach with Ring cameras</a></li>
</ul>


<!-- Product Review section -->
<hr class="major" />

![](assets\images\logo\smartthings.png){:.image.dan-left}

## DIY Security System using SmartThings

**You can use your existing SmartThings hub and sensors to create a simple security system with little to no additional investment, but there are several deficiencies that prevent it from being a mostly hands-off experience.**  I used the Smart Home Monitor and SHM Delay SmartApps, along with a few devices (Fire tablet, ActionTiles license, Konnected module, power converter, cables) to get a makeshift system. The amount of work I put into building and testing the system, and the annoyances I’ve yet to fix made me realize the worth of a professional security system like Ring. 

<p class="box">
<i>The arming and disarming of a security system can be automated with a presence sensor. Please check out my section on <a href="{{ 'presence-sensor.html' | absolute_url }}">Presence Sensors</a> for more info.</i></p>


<figure class="align-center">
 <a class="image-link" href="assets\images\other\diy-security.jpg" ><img src="assets\images\other\diy-security.jpg" alt="" /></a>
 <figcaption>
I wall-mounted a tablet where the alarm keypad used to be. Easy to do with less risk compared to directly wiring the tablet to a power source.
 </figcaption>
</figure>

Without an automated method to arm and disarm the system, I installed a wall-mounted tablet so I could arm the system before I left the house. I used an old LG  tablet ($35), an ActionTiles license ($25), and some cables and converters ($11) to mount the tablet. 

### The Problems

The **``SHM Delay``** app is critical for a working DIY security system, as the Smart Home Monitor in SmartThings doesn’t have basic features like entry/exit delays (really??). 
I spent days tweaking the **``SHM Delay``** app but still run into false alarms. I’m sure it’s not working correctly due to my mistakes, but the fact that I’m spending hours out of my day  to fix it is enough for me to switch to a professional system.

Once I was able to get a working system in place, I started thinking about the ways the system could fail.  What if the tablet stops responding and I can’t disarm the alarm? What if someone smashes the siren or disconnects SmartThings?  What if SmartThings servers go offline? I eventually realized the harsh truth that these devices aren’t designed to be a security system and don’t have the safeguards to protect my home.  In the end, I disabled the siren and added a camera in the living room. I now rely on my phone for intrusion alerts, which I hope I am awake to respond to it. 

<p class="box">
<i>If your home already has a pre-wired security system, you can use a device called <a href="{{ 'contact-sensor.html#konnected' | absolute_url }}"> Konnected ($89)</a> to use the wired sensors in home automation hubs like SmartThings. The downside is you’re still stuck with the limitations of a DIY security system that I described.</i></p>

### Installation and Smart Home Integration

It's possible to connect the SmartThings security solution and Home Assistant together using MQTT and this [SmartApp](https://ethitter.com/2016/08/smartthings-smart-home-monitor-shm-mqtt-home-assistant/) from user @ethitter.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/diy-security-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>TBD
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice:</strong> <br>I couldn't get SHM to work with Google Assistant.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/diy-security-st.png"  />
      <figcaption>
        <strong>SmartThings:</strong> <br>TBD
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/diy-security-app.png"  />
       <figcaption>
         <strong>SmartThings App:</strong> <br>TBD
       </figcaption>
      </figure>
	</div>
</div>
<p></p>


<!-- Product Review section -->
<hr class="major" />

## Self Installation with Professional Monitoring

![](assets\images\product-photo\simplisafe.jpg){:.image.dan-left}

### Simplisafe

**If you don’t mind having duplicate sensors for home automation and security, then a dedicated security system is the most reliable way to securing your home.** My friend was looking for such a system, so I suggested Simplisafe, based on the [Wirecutter’s recommendation](https://thewirecutter.com/reviews/the-best-home-security-system/). If I were to do it all over again, I’d try out Ring Alarm, but my experience with Simplisafe has been nothing but excellent—besides the expensive monitoring cost.  

Simplisafe offers a security camera which works as described, but isn’t useful without their $25/month monitoring service, as you don’t have access to the mobile app to view the camera feed.  Visual verification is an exclusive feature to Simplisafe that allows the monitoring center to access your camera feed and verify an intrusion, though it maybe not worth the privacy risk, especially after the recent [Ring incident](https://gizmodo.com/amazons-ring-security-cameras-may-have-let-employees-sp-1831658669). The variety of security sensors available is unmatched—you can buy an (really loud 105db) siren, key fob, keypad, panic button, glass break sensor—which aren’t available on Ring yet. 

I haphazardly tested a few features based on what I could reasonably test without setting off police alerts. Upon unplugging the hub, an e-mail alert was sent within seconds—that is insanely fast!  The door sensors have been accurate so far, and the motion sensors are more responsive than the Z-wave ones I use—it even detected motion while I was crawling on the floor. If you don’t want pets to set off the alarm, you can rotate the sensor upside-down so the sensor can only sees straight ahead and towards the ceiling.

### The Problems

Where Simplisafe fails is the high monthly price for critical functions. Yes, it was a dick move to hide access to the mobile app behind the $25/month tier. Simplisafe is trying to increase the value of the tier by including free camera storage, but that is a ploy to purchase their unproven indoor and doorbell cameras.  The price tag stings even more when compared to Ring’s $10/month service, which offers the same 24/7 monitoring, cellular backup, plus free storage of camera footage history.

I also wish someone figured out how to use Simplisafe sensors with Home Assistant. They operate on a proprietary RF frequency and only communicate to the Simplisafe hub, unfortunately.

### Installation and Smart Home Integration

Installation is a breeze as the included sensors are already paired with your system if you purchase a set. The box that holds the sensor has a serial # listed, which will help you identify the sensor in the system and rename it to something more appropriate, like **Front Door**.

Home Assistant integration exists with Simplisafe but is limited to a virtual alarm control panel, which not very useful as you can you have many other options (key fob, keypads) to disable the alarm.

Google Assistant integration exists to arm the system. Disarming through voice command is not allowed for security reasons. You don’t want a burglar breaking in and using his voice to disarm the system.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/other/simplisafe-ha.png" />
        <figcaption>
            <strong>Home Assistant: Okay</strong><br>Cannot use Simplisafe sensors, only control panel.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
          <strong>Voice: Okay</strong><br>You can arm the system, but not disarm through voice. 
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
       <img src="assets/images/integrations/na.png"  />
       <figcaption>
         <strong>Simplisafe App: Okay</strong><br>tbd
       </figcaption>
      </figure>
	</div>
</div>
<p></p>



<!-- Product Review section -->
<hr class="major" />

## The Competition

<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\product-photo\abode.jpg" alt=""/>
        <figcaption>Abode</figcaption>
      </figure>
      <h3>Abode</h3>
      <p>There are professional security systems that can integrate with Home Assistant, but the home automation platform will be unstable using Home Assistant. If this is still the route for you, one option is to pair the Abode security system with Home Assistant, allowing Abode’s sensors to be recognized as Home Assistant entities. The <strong>Abode</strong> component communicates over the internet but hasn’t caused noticeable delays, according to a Reddit user I spoke with. The problem with this approach is that it relies on Home Assistant as the home automation platform, which isn’t stable enough to be left unattended. </p>
      <p>If you plan to start with simple lighting automations, then look into Abode’s recently released automation engine, <strong>Cue</strong>. It seems simple and easy to use, though I wouldn’t expect it to handle complex automations. The downside is that your Z-Wave devices must be compatible with Abode, which is not always the case.</p>
    </div>
    <div class="6u$ 12u$(small)">
	    <figure class="align-left">
          <img src="assets\images\product-photo\ring.png" alt=""/>
        <figcaption>
          Ring
        </figcaption>
        </figure>
		<h3>Ring Alarm</h3>
		<p>And the wait is over! After a lawsuit from ADT that delayed the release of Ring's alarm system, it is finally here. And just recently, some Home Assistant users developed a <a href="https://community.home-assistant.io/t/ring-alarm-mqtt-discovery-alarm-integration/88070"> Hass.io add-on</a> that integrates Ring's contact and motion sensors with Home Assistant. That means you can use Ring sensors for any home automation. I have trouble finding reliable Z-Wave sensors, so I would gladly go with Ring sensors.</p>

        <p>Ring is the best home security system -- it is the most affordable security system available and has most, if not all the key features that consumers need. Glass break sensors aren’t available with Ring, but using the new Alexa Guard feature with current-generation Amazon Echos can replicate that ability. Professional 24/7 monitoring starts at $10/month, which is the lowest price in the market.</p>
    </div>   
</div>
