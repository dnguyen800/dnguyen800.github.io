---
layout: page
title: Smart Locks
short_title: smart-lock
excerpt: You'll never be locked out of the house again with a smart lock, unless you forget your phone. Then that's all on you.
competitors: "August, Schlage, Next x Yale"
update: "<strong>April 15, 2019:</strong> Added review of the August smart lock."
permalink: /smart-lock
image: assets/images/overlay-ws/smart-lock.jpg
image_credit: Dan Nguyen
categories: 
    - "Security"
    - "Home Automation"

---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\august.png){:.image.logo} 
|:-:
| **August Smart Lock Pro** 

## What you need to know

**Whenever people ask me about smart locks, I ask them why they think it’s needed.** The lack of an immediate response shows they haven’t considered the benefits or, more importantly, the risks that come with adding a smart lock to your home. It is easy to forget that the lock may be the only security measure standing between your home and an intruder, so don’t just buy a lock without a plan! Let’s start by learning what smart locks can do.

Like with most smart home items, the main draw of smart locks is convenience. Imagine never having to lock the door as it locks itself after you leave the house. There are times when I left the door unlocked and wished I had a smart lock, instead of stressing out over a potential break-in. Smart locks can be useful when you need to provide temporary access to dog walkers, visiting relatives, and friends.  Like with smart garage door openers, smart locks can grant peace of mind that the door will always be locked. 

A smart lock adds convenience but also risks. If you do end up getting a smart lock, be sure to add a security camera as an extra detective measure for unauthorized entries. If someone unexpected arrives and bypasses the lock (maybe he snuck in right as you left the house, before the lock activated), the camera should alert you of his presence. Here are some plausible scenarios where a smart lock adds risk to your home:

- The house remains unlocked for a period of time due to an automation, hub or presence sensor issue.
- The smart lock is physically unlocked but reports as locked in the app. 
- Someone gains unauthorized access to SmartThings or Home Assistant (through a security vulnerability, or improperly exposing instance to the internet) and can control the lock.

<figure class="align-center" style="width: 50%;">
 <a class="image-link" href="assets\images\other\august-install.jpg" ><img src="assets\images\other\august-install.jpg" /></a>
 <figcaption>
Removing the latch of a single bolt lock.<strong>| August</strong>
 </figcaption>
</figure>
<p></p>

All smart locks require some disassembly of the current lock, so renters will need permission before making changes. The August Lock is the least intrusive installation, as it replaces only the thumb latch found on the door facing inside the home. Your landlord won’t notice the change unless he/she regularly enters your apartment—just remember to re-install the original parts when you move out.

### Considerations before buying a smart lock

<ul class="alt">
  <li>Ask yourself whether a lock is worth the additional risk.</li>
  <li>A lock may not properly lock due to the door jamming from weatherstripping or strike plate alignment. </li>
  <li><strong>Does it support Z-Wave or require an additional hub?</strong> Using another hub presents additional security risks, and the app may go unsupported in the future. </li>
  <li><strong>Will it fit your door?</strong> Check if your lock is a single bolt or double bolt configuration. Is the door handle on the left or right side?</li>
  <li>Do you have additional security measures in case your smart lock is compromised?</li>
  <li>Thoroughly test automations if you plan to automate locking/unlocking.</li>
</ul>

### What you get with a smart lock

<ul class="alt">
  <li>Unlock the door with your phone. Now you can go jogging without your keys.</li>
  <li>Get alerts of doors left unlocked.</li>
  <li>Give guests temporary access to the house with their own unique code or account.</li>
  <li>Lock your door automatically when you leave the neighborhood.</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2WRHjjX">August Lock Pro</a> on Amazon</li>
  <li><a href="https://community.home-assistant.io/t/august-smart-lock-pro-zwave/28654/42">Forum post</a> including tips on connecting the August Lock Pro to Home Assistant</li>
  <li>How to add Z-Wave network key in <a href="https://www.home-assistant.io/docs/z-wave/adding/">Home Assistant</a></li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
       <img src="assets\images\product-photo\august.jpg" alt=""/>
       <figcaption>
         Smart Lock Pro <strong>|  August</strong>
       </figcaption>
</figure>

## August Locks

**If you want to try out a smart lock but don’t own a home, then August locks might be the solution for you.** Keep in mind that some disassembly of the current lock is required, so it is your responsibility to follow the rental agreements. August locks only require replacement of the thumb latch, so the lock replacement is unnoticeable from the outside and your (and landlord’s) existing keys will continue to work. I recommend the August Lock Pro for its **``Z-Wave support``**, so you can avoid using the poorly-reviewed August app and Connect Wi-Fi Bridge.

**August locks only work on single bolt locks.** I wasn’t familiar with the term, but luckily August has a nice illustration (see below) to explain the difference.

<figure class="align-center" style="width: 50%;">
 <a class="image-link" href="assets\images\other\august-compatibility.png" ><img src="assets\images\other\august-compatibility.png" /></a>
 <figcaption>
August locks can only be installed on single bolt doors. <strong>| August</strong>
 </figcaption>
</figure>

I've read on deal and home automation forums that the battery life on August locks is poor, lasting only a few months. This would normally be bad, but the lock uses four AA batteries that are easily interchangeable by removing the front cover. I prefer this approach because battery replacement is so easy, but maybe not good for residences that aren't within driving distance.

### The Problems

I never tested the included August Connect Wi-Fi bridge, which lets you unlock from anywhere with an internet connection.  I’ve only read bad reviews about it, so I ended up selling it after I had the Z-Wave connection working with the August Pro. 

For security reasons, I don’t automatically lock the door using geolocation. Instead, I use SmartThings notifications as a shortcut to open the app and unlock the door. I haven’t run into any issues with the door unlocking when it wasn’t supposed to, but I only tested for a few days. 

### Installation and Smart Home integration

**Check if your lock is a single bolt lock, as that is the only lock type compatible with August locks.** You should also check your door area for any potential jamming from weather stripping or strike plate misalignment. If you need to nudge the door forward or wiggle the key in a certain way in order to open the door, then the August lock will have issues. I installed an August Lock Pro on the garage entry door and it took one hour two hour for a first-time install. 

The Smart Lock Pro supports **``Z-Wave``**, so connecting to SmartThings was incredibly easy -- I won't explain how to do it here. Connecting to Home Assistant took several hours of researching because I had not defined a network key in my Z-Wave configuration to do secure inclusions and so the lock was detected as an unknown device. After defining a network key in the **``configuration.yaml``** and **``options.xml``**, it pairs correctly as a smart lock.

Designing automations in Home Assistant took much more time to get it right, as I had to first find a timely and accurate presence sensor first. Read about my recommendations [here](presence-sensor.html).

Google Assistant is supported through the August Connect bridge or by association through SmartThings and Home Assistant integration. I haven't tested yet, but you can't say the phrase “lock the front door in x minutes” yet.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/august-lock-ha.png" />
        <figcaption>
          <strong>Home Assistant: Average</strong><br>Quite difficult to connect to Z-Wave hub. Required setting up the network key, which didn't work at first. 
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
			<strong>Voice: Good</strong><br>Works through SmartThings. I wish I could say "lock in x minutes."
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
        <strong>SmartThings: Great</strong><br> Easily pairs to SmartThings as a Z-Wave lock.
      </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/august-app.png"  />
       <figcaption>
         <strong>August App: Great</strong><br>Simple, easy-to-use.
       </figcaption>
      </figure>
	</div>
</div>

<p></p>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
       <img src="assets\images\product-photo\schlage-keypad.jpg" alt=""/>
       <figcaption>
         Schlage keypad lock <strong>|  Schlage</strong>
       </figcaption>
</figure>

## Schlage Keypad Locks

Schlage Keypad Locks can offer most of the conveniences of a smart lock, but avoids certain risks and is slightly cheaper. A four-digit code is all that’s needed to unlock, and you have the multiple key codes available for guests. It’s inconvenient to revoke access by changing the keycode, but that is a problem most people will rarely deal with.

You don’t have to worry about remotely locking the door, as the door always locks when closed. You lose the ability to receive notifications when the door is unlocked, but that can be replaced with a camera or door sensor.

### Installation and Smart Home Integration

If you’re a renter, you can’t install the lock as it replaces the entire door handle and requires a new set of keys.  The lock is powered by a 9V battery that lasts quite long—my battery is going strong for over a year.