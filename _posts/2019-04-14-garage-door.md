---
layout: page
title: Garage Door Openers
short_title: garage-door
excerpt: If a house had a butt, it would be the garage.
competitors: "Chamberlain/Liftmaster MyQ, Aladdin Genie, Linear GoControl, Gogogate, Garagemate"
permalink: /garage-door
image: assets/images/overlay-ws/garage-door.jpg
image_url: https://unsplash.com/@ralphkelly
image_credit: Ralph Kelly via Unsplash
categories: 
    - "Gadgets"
    - "Home Automation"
---

<!--more-->

#### I personally tested the following:

|---
| ![](assets\images\logo\chamberlain.png){:.image.logo}
|:-:
| **MyQ Smart Garage Door Opener/Hub (MYQ-G0301)**<br>**MyQ Internet Gateway Garage Door Opener (CIGBU-P)**


## What you need to know

A smart garage door opener is a useful gadget that adds convenience, additional security, and in some cases, saves money. There is less of a chance that you accidentally leave the door open, as the mobile app will alert you if that happens. If you want to get advanced with door openers--such as automatically opening the garage door when arriving at home--there is a lot of testing involved on your end to make sure the automations work as expected and don’t accidentally open the garage door at midnight.

Besides helping with forgetfulness, there are other useful ways to use a connected garage door and a phone. For starters, your phone becomes a garage remote. Going for a neighborhood jog no longer requires bringing along a set of keys if you have your phone with you. In a house with several roommates and not enough garage remotes, a smart garage opener makes it easy to add and revoke access with a few presses on the mobile app. It is very convenient to have a smart garage opener, but it also exposes your home to additional risks.

### Security considerations

Before getting into details of garage door automations, it is important to emphasize security and potential exposures when adding a smart garage opener. You are adding an Internet-dependent device (unless you use a local Z-Wave controller) that can remotely open a door to your home. It’s possible that the Chamberlain IT admin abuses his privileges and accesses your account, or a hacker exploits vulnerabilities in the garage opener app to gain physical access to your home.  It is good to have preventative and detective measures in place to reduce these risks. Segregating network devices using VLANs, remove old or unnecessary devices from the network, disabling router settings like UPNP, and updating device firmware are some practices I suggest, though it’s better to do your own research as best practices and threats continue to change.

When designing automations using garage openers and presence sensors, I recommend to keep it simple and use app notifications that notify when entering/exiting an area, instead of automations that automatically open and close the door without intervention. Presence sensors are not always predictable or timely, meaning it could take several minutes before the sensor detects you are away and closes the garage. Sometimes it only takes a few minutes for someone to break into your home and it would be much easier with a poorly designed automation.

### Considerations before buying a smart garage opener

<ul class="alt">
  <li><strong>Consider the security risks added to the benefits gained.</strong> Is it worth it? Do you have other mitigating controls?</li>
  <li><strong>Check if your garage door is compatible with a smart opener.</strong> Chamberlain, Liftmaster, and some Genie and Craftsman garage doors work with MyQ. Other garage doors can use GoControl Z-Wave Opener or Garagemate.</li>
</ul>

### What you get with a smart garage opener

<ul class="alt">
  <li>A garage remote on every phone you own.</li>
  <li>Grant and revoke garage door access to household members easily through the MyQ app.</li>
  <li>Setup voice and mobile app notifications if the garage is open for a period of time, while away, etc.</li>
  <li>Use a voiec assistant to open the garage door.</li>
  <li>Open or close the garage from your car (assuming your phone is connected to your car and voice assistant is set up).</li>
  <li>If you lock yourself out but have your phone with you, then you can open the garage!</li>
</ul>

### Recommended Reading
<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2Xarx7x">MyQ hub</a> on Amazon</li>
  <li> Connect MyQ to <a href="https://community.smartthings.com/t/release-myq-lite-door-and-lamp-control-for-liftmaster-chamberlain/49150">SmartThings with custom device handler</a> and <a href="https://www.home-assistant.io/components/myq/">Home Assistant component</a>.</li>
  <li>MyQ garage <a href="https://support.chamberlaingroup.com/s/article/List-of-compatible-garage-door-openers-for-MyQ-Garage-1484145635905">compatibility list</a>. Surprisingly, it works with some Craftsman and Genie garage doors.</li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
  <img src="assets\images\product-photo\myq.jpg" alt=""/>
  <figcaption>
    The MyQ Hub (MYQ-G0301) |  <strong>Chamberlain</strong>
  </figcaption>
</figure>

## Chamberlain MyQ

**With few reliable options to choose from, the [MyQ Smart Garage Hub](https://amzn.to/2Xarx7x) is your best option if you have a compatible Chamberlain, Liftmaster, Craftsman or Genie garage.**  MyQ doesn’t earn my full recommendation because of their nickel-and-dime practices of charging money for basic features like voice assistant, but other than that, the MyQ hub and mobile app works as expected and is easy to install. MyQ is a Chamberlain product, so it works with the majority of Chamberlain and Liftmaster garages commonly found in the U.S.

The MyQ app has most of the features I would expect. You can set up notifications to alert you when a garage door is opened, or if a garage has been open for more than a number of minutes. Chamberlain finally added the ability to share access with multiple users, so I no longer have to share an account with my roommate. There is no **home/away assist** feature that automatically opens and closes the garage door -- it is probably too much liability for Chamberlain to have that feature if it behaves improperly. 

<figure class="align-center" style="width:35%;" >
 <a class="image-link" href="assets\images\product-photo\myq.png" ><img src="assets\images\product-photo\myq.png"  /></a>
 <figcaption>
The older version of the MyQ gateway (CIGBU-P) that can be found for cheap, around $35.
 </figcaption>
</figure>

The current model sold today is the **MyQ Smart Garage Door Opener/Hub (MYQ-G0301)**. This model supports more garage door openers and uses Wi-Fi, which gives you more leeway where the hub can reside in the garage. The previous model, **MyQ Internet Gateway Garage Door Opener (CIGBU-P)**, can be found on eBay for cheap--around $35. It doesn't use Wi-Fi, and if bought used, may require a call to Chamberlain tech support to reset the device and wipe the previous owner's garage code. I had to do this once, and honestly, it's not worth the hassle to save $30.


### The Problems

The MyQ device relies on an internet connection and MyQ servers to function, which opens up additional security risks. We don't know how secure the app is, or how Chamberlain monitors administrator access. The official integration of MyQ with services like IFTTT, Alexa and Google Assistant requires a $5/month subscription to MyQ. I use unofficial integrations as a loophole to the fee, but Chamberlain could shut it down at any time.

If you connect a MyQ account that has only guest access to garage doors, then you will not be able to access those doors in SmartThings or Home Assistant. As the guest account is a new feature in MyQ, it's possible the integrations will be updated to support it, but that hasn't happened yet.

### Installation and Smart Home Integration

The MyQ app guides you through the physical and software installation of the hub.  Place the MyQ hub near the garage opener, press the **``Learn``** button on the garage opener, and then follow instructions on MyQ app.

The MyQ app was recently updated to add guest access to a home. Now you don't have to share one user account to open the garage. Users with guest access cannot use their accounts in the SmartThings and Home Assistant integrations though--the main MyQ account needs to be used.

Unofficial MyQ integrations with [SmartThings](https://community.smartthings.com/t/release-myq-lite-door-and-lamp-control-for-liftmaster-chamberlain/49150) and [Home Assistant](https://www.home-assistant.io/components/myq/) exist but could stop working if MyQ changes how it handles communications. For SmartThings, an additional [tilt sensor](tilt-sensor) is needed to work properly with the custom device handler. For Home Assistant, you only need to enter your credentials for access (which is slightly concerning).  It works with voice assistants that are paired with SmartThings and Home Assistant. 


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/myq-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Requires saving plaintext MyQ credentials in HA configuration, which is a bit concerning. 
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Okay</strong><br>Pair MyQ with Smartthings with ST device handler to avoid paying Chamberlain's monthly fee. Works as expected.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
      <img src="assets/images/integrations/myq-st.png" />
      <figcaption>
      <strong>SmartThings: Good</strong><br>Requires ST device handler, but works fine after that. Additional tilt sensor required for accurate reporting of door status.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/myq-app.png" />
       <figcaption>
         <strong>MyQ App: Good</strong><br>Easy to setup common garage door notifications. You can now share access with other accounts (finally).
       </figcaption>
      </figure>
	</div>
</div>