---
layout: page
title: Tilt Sensors
short_title: tilt-sensor
excerpt: Probably the most useless item on this site. Don't even bother reading this article. 
competitors: "Monoprice. Not much else."
permalink: /tilt-sensor
image: assets/images/overlay-ws/sensors.jpg
image_credit: Dan Nguyen
categories: 
    - "Sensor"
    - "Security"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\monoprice.png){:.image.logo} 
|:-:
|**Z-Wave Plus Acceleration Sensor**


## What you need to know

Tilt sensors operate differently than door/contact sensors in that it is made of a single piece (versus two pieces for door sensors) and detects movement through gravity and acceleration. It’s easier to understand with the picture below.

<figure class="align-center" style="width:60%;">
 <a class="image-link" href="assets\images\other\tilt-sensor.png" ><img src="assets\images\other\tilt-sensor.png" /></a>
 <figcaption>
How a tilt sensor works. <strong>| randomnerdtutorials.com </strong>
 </figcaption>
</figure>

It is basically a small ball in a tube that touches the end of the tube to complete the circuit flow! The most obvious movement it can detect is when a garage door moves from a vertical position **``closed``** to a horizontal position **``open``**. A typical door sensor is difficult to use with garage doors due to the gap between the door and wall being too wide—this is where a tilt sensor becomes useful. I previously used a tilt sensor with the **Chamberlain MyQ garage door opener** to get an “accurate” reporting of garage door status, though I stopped using it due to unreliable status reporting. It seems that this is a common theme with tilt sensors like the Ecolink sensor, but there are workarounds mentioned in [Amazon reviews.](https://www.amazon.com/Z-Wave-Plated-Reliability-Garage-TILT-ZWAVE2-5-ECO/dp/B01MRZB0NT/ref=sr_1_1?keywords=ecolink+tilt&qid=1553801492&s=gateway&sr=8-1#customerReviews)

A tilt sensor for the garage door wouldn’t be necessary if Chamberlain allowed users access to the MyQ data outside of the app. A tilt sensor is meant to be an extra verification that the door is in fact, closed. With the poor reliability of the tilt sensor I used, I would rather rely on a camera to confirm the door is closed.

### Considerations before buying a tilt sensor

<ul class="alt">
  <li><strong>RF signals may be absorbed by a metal garage door.</strong> Try to place a portion of the sensor away from the door, like what this Amazon reviewer did. </li>
  <li><strong>Consider the position of the sensor on the garage door—and don’t place it at the bottom of the door.</strong> When the door opens, the sensor should begin rotating immediately with the door.</li>
  <li><strong>Random, false positives from the sensor are possible</strong>, so I don’t recommend setting up alarm automations until thoroughly tested.</li>
  <li><strong>Some remote garage openers include a tilt sensor,</strong> like the Linear GoControl Z-Wave Garage Door Opener, so you don’t need to buy a separate sensor.</li>
  <li></li>
</ul>


### What you get with a tilt sensor

<ul class="alt">
  <li>Additional confirmation that the garage door is closed, though it’s not 100% accurate without workarounds.</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li>Installation tips from <a href="https://www.amazon.com/Z-Wave-Plated-Reliability-Garage-TILT-ZWAVE2-5-ECO/dp/B01MRZB0NT/ref=sr_1_1?keywords=ecolink+tilt&qid=1553801492&s=gateway&sr=8-1#customerReviews">Amazon.com reviewers</a></li>
</ul>

<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
 <img src="assets\images\product-photo\monoprice-tilt.jpg" alt=""/>
   <figcaption>
          The Monoprice tilt sensor <strong>| Monoprice</strong>
   </figcaption>
</figure>

## Monoprice Z-Wave Plus Acceleration Sensor

**The Monoprice Z-Wave Plus Acceleration Sensor sucks, period. Don't buy it.** If a sensor is accurate only 80% of the time, then it's not worth it. I was getting the worst kind of false positives where the garage door is physically closed, but the sensor reported it as open. That is unacceptable when I’m away from home for days at a time and can’t confirm the door is closed, which is the sole purpose of a tilt sensor. The placement of the sensor on the garage door only needs to report status in two positions: horizontal or vertical. I don’t know how the sensor can report those states incorrectly so often, but it does. 

There are potential workarounds mentioned on Amazon reviews of the Ecolink tilt sensor, but I already stopped using the sensor by that point. My sensor was placed on the top panel of the garage door, but still had problems detecting vertical and horizontal position. I gave up on the sensor and installed a camera to check the garage door if needed. I haven’t had to use it as MyQ has been reporting status correctly without the sensor.