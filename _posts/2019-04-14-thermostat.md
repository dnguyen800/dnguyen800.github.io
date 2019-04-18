---
layout: page
title: Thermostats
short_title: thermostat
excerpt: For the few times I actually used a smart thermostat, I couldn't imagine living without one.
competitors: "Nest, Ecobee, Honeywell, Emerson"
permalink: /thermostat
image: assets/images/overlay-ws/thermostat.jpg
image_credit: Dan LeFebvre on Unsplash
image_url: https://unsplash.com/@danlefeb
categories: 
    - "Gadgets"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\nest.png){:.image.logo} |  ![](assets\images\logo\ecobee.png){:.image.logo} 
|:-:|:-:
| **Nest 3rd Gen** | **Ecobee 3**<br>**Ecobee 4** 


## What you need to know

The one time when my smart thermostat showed its value was on an especially cold night--I finished eating dinner at a restaurant and was sitting in my car, knowing I would be driving home to a freezing cold house. 

The thought of it wasn't appealing, but that was when I realized I could open the Nest app on my phone and crank up the thermostat temperature remotely. Instantly, the cold thoughts in my mind melted away, and I was excited to head home. That feeling of entering a warm house after spending hours in the cold was like taking a hot a shower after days of sweaty hiking—it was amazing—the very definition of comfort.

Living in California, I rarely use a smart thermostat to its full potential, but I can see the value for others. For people who regularly use the furnace, a smart thermostat will warm up the house  at the right times and electricity cost will be slightly less than without a smart thermostat. If you live in a colder climate where chilly nights are frequent, then the thermostat’s value definitely shows. For instance, you can use a Nest thermostat to heat up the house and prevent pipes from freezing and bursting. If you’re a frugal person who never turns on the thermostat in the first place, then there is no benefit to be gained here.

Smart thermostats like Nest and Ecobee regularly go on sale so it’s easy to snag one at a reasonable price of $170.

### Considerations Before Buying A Smart Thermostat

<ul class="alt">
  <li><strong>Use the <a href="https://nest.com/works/">Nest compatibility checker</a> to see if your home’s existing wiring is compatible.</strong></li>
  <li><strong>If you have two thermostats and two separate zones, you may need two smart thermostats.</strong> Some furnaces cannot maintain dual temperatures that vary too widely. Having the first floor at 60°F and the second floor at 70°F may put too much strain on your system.</li>
</ul>


### What You Get With a Smart Thermostat

<ul class="alt">
  <li>Warm up or cool down the house before arriving at home.</li>
  <li>Forget about adjusting the thermostat—the home/away assist feature on the mobile app turns off the thermostat for you.</li>
  <li>Get safety alerts and reminders, like extremely cold weather, to turn on the heating.</li>
  <li>The thermostat learns your behaviors, like if you tend to turn on the heater after waking up.</li>
  <li>Give roommates control of the thermostat via the app, if they cannot physically access it.</li>
  <li>Change the thermostat temperature while staying cozy in bed.</li>
</ul>


### Recommended Reading

<ul class="alt">
  <li><strong>Affiliate link:</strong> Purchase the <a href="https://amzn.to/2D2Ap3Y">Nest thermostat</a> or <a href="https://amzn.to/2uPujPG">Ecobee</a> on Amazon</li>
  <li>Thermostat Compatibility Checker for <a href="https://nest.com/works/">Nest</a> and <a href="https://www.ecobee.com/compatibility/">Ecobee</a></li>
  <li>Integrate the Nest thermostat with <a href="https://community.smartthings.com/t/release-nst-manager-v5-0/83228">SmartThings with custom device handler</a> and <a href="https://www.home-assistant.io/components/nest/">Home Assistant component</a></li>
  <li>Integrate Ecobee thermostat with <a href="https://support.smartthings.com/hc/en-us/articles/208005686-How-to-connect-ecobee-thermostats">SmartThings</a> and <a href="https://www.home-assistant.io/components/ecobee/">Home Assistant</a></li>
</ul>


<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
  <img src="assets\images\product-photo\nest-thermostat.png" alt=""/>
  <figcaption>
    The Nest 3rd Gen <strong>| Alphabet, Inc.</strong>
  </figcaption>
</figure>

## Nest Thermostats

**I recommend any smart thermostat currently on sale, which is usually the Nest E. It has all important features of the Nest 3rd Gen, but regularly goes on sale for $130 or less.** Get the Nest 3rd Gen for $180 if you want a nicer looking, metal finish on your thermostat. Ecobees are just as good as Nest, so there is no wrong choice here.

Honestly, there is not much to rave or complain about -- the Nest is what you expect out of a smart thermostat. The Nest app is straightforward to use, and according to [this security study](https://www.tomsguide.com/us/smart-home-leaky-apps,news-29319.html) of smart home apps, Nest is one of the few apps that encrypts communication between the thermostat and Nest app, even when on the same local network. 

### The Problems

There aren't any major problems with Nest, but the **Home/Away Assist** feature can be very slow to detect presence changes. I've compared Nest times to actual times and have seen hour-long gaps in detection. I've also arrived home to see that the Nest cameras remained on (should be off when someone is home) and the thermostat not adjusted. If you want to come home to a warm house, the most reliable way is to use the Nest app before heading home.

### Installation and Smart Home Integration

Physical installation is not difficult, but you need to use the <a href="https://nest.com/works/">Nest compatibility checker</a> if your home’s existing wiring is compatible. I had to call tech support once because there were more wires in my existing installation than what was covered in the installation guide. Physical installation requires some basic do-it-yourself **DIY** skills like drilling holes and basic electrical wiring.

Nest thermostats come with a wall plate to cover the gaping hole left by the previous thermostat. How nice!

Connecting the Nest to SmartThings uses an unofficial SmartApp called [NST Manager](https://community.smartthings.com/t/release-nst-manager-v5-0/83228). It's not difficult to set up, but requires creating a Nest developer account, using the SmartThings developer portal to add a SmartApp. As an unofficial integration, it's quite impressive to have the thermostat and  cameras working in SmartThings. Kudos to the team.

The **Home/Away Assist** feature on the Nest app is not timely, so the other option you have is to use voice control, say, in the car driving home, to warm up the house before you arrive. 

Very rarely do I need to change the temperature, so home automation integration is not all that important to me. I find that using the app is the most convenient way to fiddle with the thermostat. But it is very easy to connect the Nest to Home Assistant. SmartThings requires the installation of a device handler, but that’s not too hard.



<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/nest-thermostat-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Requires a free Nest developer account. Looks great in HA!
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
      <strong>SmartThings: Good</strong><br> Tedious one-time setup. Requires developer account and device handler setup.
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


<!-- Product Review section -->
<hr class="minor" />

<figure class="align-left">
  <img src="assets\images\product-photo\ecobee-thermostat.png" alt=""/>
  <figcaption>
    The Ecobee4. <strong>| Ecobee</strong>
  </figcaption>
</figure>

## Ecobee Thermostats

I have a confession to make: I only purchased the Ecobee instead of Nest because it was currently on sale. I read comparison articles but didn't find many notable differences between the two, so I went ahead and bought it for my friend. 

**And lo and behold, the Ecobee is just as good as the Nest but it is better in a few ways.** It officially supports SmartThings and is easy to set up. The Ecobee also includes room sensors, which can also act as really slow room occupancy sensors. In a large house where temperature varies greatly, I can see this being useful, but not a must-have. 

Both the Ecobee 3 and Ecobee 4 are still available for sale. The only difference I noted was the inclusion of Amazon Alexa on the Ecobee 4, which I found to be a useless feature. The location of my thermostats are in low traffic areas (hallways, stairs), and there was rarely a time when I needed Alexa to do something while standing in the hallway. If I do, I end up yelling and the wrong Echo speaker picks up my request. So I'm still unsure why I paid extra money for this feature.

### The problems

I haven't encountered any major problems to note. Once, the Ecobee/SmartThings integration broke and I had to log in again. I have not tested the accuracy of the Home/Away feature, but I don't think it will be any better than Nest, so expect delayed updates up to an hour. If you want to come home to a warm house, you will (still) need to use the app.

### Installation and Smart Home Integration

The installation process is just as easy as Nest--all steps are covered in the app. Labels are included for the thermostat wires. There is a compatibility checker section on the Ecobee app to guide Physical installation requires some basic do-it-yourself **DIY** skills like drilling holes and basic electrical wiring.

Connecting the occupancy sensors to the Ecobee is incredibly easy. Just remove the tape from the battery and the thermostat will detect the sensor and confirm with you to add to your home.

Ecobee is officially supported by SmartThings and integrates easily using a SmartThings SmartApp. Integrating with Home Assistant requires a developer account, which is free.

Comes with a wall plate to hide the hole or any visible wires.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/ecobee-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Create a developer account and add to your config. Looks great!
        </figcaption>
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