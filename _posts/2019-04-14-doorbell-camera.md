---
layout: page
title: Doorbell Cameras
short_title: doorbell-camera
excerpt: Do you want to know when and how your package was stolen? Get a doorbell camera.
permalink: /doorbell-camera
competitors: "Nest, Ring, Securisafe, Laview"
image: assets/images/overlay-ws/doorbell-camera.jpg
image_credit: Dan Nguyen
categories: 
    - "Camera"
    - "Security"
    - "Home Automation"
---

<!--more-->



#### I’ve personally tested the following:

|---
| ![](assets\images\logo\nest.png){:.image.logo} 
|:-:
| **Nest Hello** 

### What you need to know

I’ve installed the Nest Hello doorbell cameras for a few friends and they all love it—I secretly believe it is because of the ability to spy on strangers passing by. The biggest selling point for me is the piece of mind knowing when and where my package was delivered. While the camera may not stop package theft altogether, at least it makes your house less of a target by being present.

Installation of doorbell cameras requires more planning, particularly with wired cameras. Consider the location and angle of the doorbell, and whether your home is equipped to support a wired doorbell.  There are solutions for nearly every scenario, though it may require a battery-operated doorbell camera.

<p class="box">
<i>Before installing a camera, it’s important to be aware of the rules and regulations regarding cameras and external installations. Living in an HOA neighborhood means you likely need approval before installing anything on the outside of your home.</i></p>

### Considerations before buying a doorbell camera

<ul class="alt">
  <li><b>Check with your HOA</b> before installing any hardware outside your house.</li>
  <li><b>Check with household members</b> about installing any cameras. Privacy should be respected, after all. </li>
  <li><b>A good wireless network is needed to avoid wireless range issues.</b> See my network router <a href="{{ 'network.html' | absolute_url }}">recommendation.</a></li>
  <li><b>Check the Nest doorbell camera <a href="https://nest.com/works/">compatibility checker</a> as not all homes are compatible with wired doorbell cameras.</b> Wireless ones (like the Ring 2) can be installed anywhere.</li>
  <li>Cameras have decent viewing angles, but check that your doorbell location is ideal for a camera. </li>
</ul>


### What you get with a doorbell camera

<ul class="alt">
  <li>Know when your packages are delivered, and potentially stolen.</li>
  <li>Know who arrives and leaves through the front door (household members, delivery people, guests)</li>
  <li>Broadcast a message to your Chromecast speakers when someone is at the door.</li>
  <li>Be notified on your phone when someone arrives at the door. </li>
  <li>Continuous recording is useful when tracking suspicious neighborhood activity.</li>
</ul>



### Recommended Reading

<ul class="alt">
  <li>The Wirecutter's recommendation for<a href="https://thewirecutter.com/reviews/best-smart-doorbell-camera/"> best smart doorbell camera</a>.</li>
  <li><b>Affiliate link:</b> Purchase the <a href="https://amzn.to/2I2RiQ3">Elago wallplate for Nest Hello camera</a> on Amazon.</li>
  <li><a href="https://nest.com/works/">Nest Compatibility Checker</a></li>
</ul>

<!-- Product Review section -->
<hr class="major" />

<figure class="align-left">
 <img src="assets\images\product-photo\nest-hello.png" alt=""/>
 <figcaption>
The Nest Hello camera. <b>|  Google</b>
 </figcaption>
</figure>

## Nest Hello

**My personal experience with the Nest Hello camera is that it is reliable at sending timely notifications, but the monthly fee is required to get any real use out of it.** Monthly fees can add up quickly, but with Nest's new $5/month plan, I think it's worth paying for reliability. Wi-Fi cloud cameras have a lot of potential points of failure (poor Wi-Fi performance, slow upload speed, crap servers) but Nest gets most of it right. I've read about too many problems with the Ring Doorbell Pro to give it a try, but I usually hear good things about Nest's doorbell camera.  I recommend it for the continuous recording, timely alerts, and a reliable mobile app. Alerts are sent to my phone within seconds, and recordings are available within a minute or two of the event. Viewing live footage takes only a few seconds too. Did I mention how quick it is to view an alert? That is really important.

### The Problems

There is a **Home/away Assist** feature on the Nest app, but I found it doesn’t work reliably. There were a few times when I received a movement alert and opened the app to see my roommate watching TV in the living room. I’ve done my own testing of the feature (Home Assistant integration gives you access to this data) and found it can take hours for Nest to update to Home or Away status.

An option to store recorded videos locally will likely never come, as every company loves subscription revenue. Power-over-ethernet (PoE) is not an option for this particular camera either. It’s either wireless or nothing with the Nest doorbell.

<figure class="align-center" style="width:50%;">
 <a class="image-link" href="assets\images\other\nest-doorbell.jpg" ><img src="assets\images\other\nest-doorbell.jpg" alt="" /></a>
 <figcaption>
The hole is quite big and can’t be covered up by the camera alone. Nest doesn't provide a wall plate.
 </figcaption>
</figure>

One surprising omission with the Nest Hello package is the lack of a wall plate. Without it, the doorbell area is exposed and the doorbell install looks unprofessional. To deal with this issue, I used the [Elago wall plate](https://amzn.to/2I2RiQ3) and can confirm it covers up the hole nicely. Considering that a wall plate is included with Nest thermostats, this is a surprising omission.

### Installation and Smart Home Integration
The wiring is easy, though first follow the [Nest compatibility checker](https://nest.com/works/) to see if your house supports wired doorbells. The hardest part of the install is physically mounting the doorbell onto a hard surface. I had to use a hammer drill and a pair of earplugs to get the job done, and I definitely annoyed some neighbors in the process.

There isn’t any usable integration with Home Assistant and SmartThings, but I think it’s better to use the Nest app to watch videos. Any footage on Home Assistant and SmartThings is a static image that is delayed by several seconds. Not very useful when trying to see who is at the door right now.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/nest-doorbell-ha.png" />
        <figcaption>
          <b>Home Assistant: Okay</b><br> It works, but impossible to see real-time footage. What is important is the ‘motion detected’ sensor.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <b>Voice: Good</b><br>Not really used, but can send broadcast messages when someone is at the door.
       </figcaption>
      </figure>
	</div>
</div>

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
        <img src="assets/images/integrations/nest-indoor-st.png" />
      <figcaption>
         <b>SmartThings: Okay</b><br> NST Manager SmartApp shows camera feed, but it's not real-time.</figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/nest-doorbell-app.png"  />
       <figcaption>
         <b>Nest App: Great</b><br>Simple, easy-to-use.
       </figcaption>
      </figure>
	</div>
</div>