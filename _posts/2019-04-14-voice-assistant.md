---
layout: page
title: Voice Assistants
short_title: voice-assistant
excerpt: I yell at my voice assistant on a regular basis, but I can't deny that using my voice to turn off the lights is convenient.
competitors: "Google Assistant, Amazon Alexa, Apple Siri"
permalink: /voice-assistant
image: assets/images/overlay-ws/voice-assistant.jpg
image_url: https://unsplash.com/@farreal
image_credit: Dan Farrell @ Unsplash
categories: 
    - "Infrastructure"
    - "Home Automation"
---

<!--more-->

#### I’ve personally tested the following:

| ![Google Assistant](assets\images\logo\google.png){:.image.logo} | ![Alexa](assets\images\logo\amazon.png){:.image.logo} | ![siri](assets\images\logo\apple.png){:.image.logo} |
|:-------:|:--------:|:---------:|
| **Google Assistant** | **Alexa** | **Siri** |

## What you need to know

A voice assistant paired with a smart home—what do you get with it?  Besides asking about the weather and setting timers, voice assistants offer another convenient way to control the lights and TV—which can be very useful when your hands are full—like when carrying groceries. 

Things get more interesting when voice assistants are linked to media services like Youtube TV, Netflix, and Hulu, but then you start to see the disparities between Google Assistant and Alexa. Though one thing that all voice assistants have in common is the amount of yelling needed for your voice to be recognized. And that’s okay—I don’t expect microphones to be any better than human ears, which already have trouble hearing me. If you factor in background noise from music, television or the kitchen, it’s a wonder that my voice is recognized at all by a voice assistant. 

When you get into the details of the supported integrations with voice assistants, you’ll quickly learn that most are not what I call **direct integrations**. For example, most integrations support Actions on Google, which requires saying **``Hey Google, ask Harmony``** to perform a task. Direct integrations are slowly being added to Google Assistant--Logitech Harmony became a [direct integration](https://www.androidpolice.com/2018/10/16/logitech-harmony-direct-control-finally-live-google-assistant-home-limitations/) in October 2018, so things will get better, slowly. My point is that training is needed on your end to learn specific phrases to use voice assistants, whether it’s using Google, Alexa, or Siri. They all kind of suck in this area.

When testing voice control with lighting, I realized that the naming convention of devices is important to avoid confusion. If I have a light strip named **TV**, a Chromecast called **Living Room TV**, and an Android TV in the living room, there’s going to be some confusion when saying **``turn off the TV``**. 

### Considerations before choosing a voice assistant
> - **Test out the voice assistants yourself** by purchasing a cheap mini speaker or using the app on your phone. 
> - **Search for keywords like “direct integration” to learn if your product supports voice assistant directly.**
> - **Consider the privacy implications of including always-on voice assistants.** I've had a few experiences where the voice assistant turned on and respond when I am 100% certain I did not say the trigger phrase.


<ul class="alt">
  <li><strong>Test out the voice assistants yourself</strong> by purchasing a cheap mini speaker or using the app on your phone. </li>
  <li><strong>Search for keywords like “direct integration”</strong> to learn if your product supports voice assistant directly.</li>
  <li><strong>Consider the privacy implications of including always-on voice assistants.</strong> I've had a few experiences where the voice assistant turned on and respond when I am 100% certain I did not say the trigger phrase.</li>
</ul>

### What you get with a voice assistant

<ul class="alt">
  <li>A hands-free way to control your lights.</li>
  <li>A basic kitchen assistant for setting timers, converting units, and more.</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li>Set up Google routines tied to your alarm clock app from <a href="https://www.howtogeek.com/406742/how-to-set-up-routines-in-google-clock-on-android/">Howtogeek</a></li>
  <li><a href="https://www.home-assistant.io/components/homekit/">The Homekit component for Home Assistant</a> opens up the Homekit platform to many unsupported devices</li>
  <li>Set up Google Assistant with <a href="https://support.smartthings.com/hc/en-us/articles/214837343-How-to-connect-Google-Assistant-with-SmartThings">SmartThings</a>, Home Assistant  with <a href="https://www.nabucasa.com/">the easy but paid way</a> or the <a href="https://www.home-assistant.io/components/google_assistant/">manual way</a>.</li>
  <li>One Amazon exclusive feature: <a href="https://www.tomsguide.com/us/alexa-guard,news-28882.html">Alexa Guard</a> can detect alarming sounds (glass break, smoke alarm) and send you a notification.</li>
  <li>How Apple anonymizes Siri requests and personal information from <a href="https://nakedsecurity.sophos.com/2018/08/13/siri-is-listening-to-you-but-shes-not-spying-says-apple/">Naked Security by Sophos</a></li>
</ul>

<!-- Product Review section -->
<hr class="minor" />

![Google Assistant logo](assets\images\logo\google-assistant.jpg){:.image.dan-left}

## Google Assistant

**If you are an Android user, it makes sense to stick with Google Assistant because of its tight integration with the Android OS, ever-expanding features and device compatibility.**  Google is ahead of the pack with its very useful Google Home app, which also has a streamlined UI that can be displayed on a tablet or phone. It is slowly replacing the functions of my SmartThings hub, though it still can’t perform any real automations that utilize sensors. One feature I love is using the **``Good Morning``** Google Routine and tying it to my phone’s alarm app. I’ve been waiting for something like that for ages!

<figure class="align-center">
 <a class="image-link" href="assets\images\other\google_home_app.png" ><img src="assets\images\other\google_home_app.png" alt="" /></a>
 <figcaption>
   A view of the Google Home app.
 </figcaption>
</figure>

Controlling the lights with Google Assistant works as you would expect if you say the full name of the light, like **living room light**. Google Assistant offer direct integration with SmartThings, so nearly every device in SmartThings can be voice controlled by Assistant, except certain actions like the disarming of alarms and locks. Things get murky when more context is needed before performing an action, but Google has a room assignment feature that helps with that. 

By assigning the light and Google Home speaker locations to their proper rooms, you can say something vague like **``turn off the lights``** and the closest Google Home speaker will turn off the lights in the room where the speaker is located in. This feature doesn’t work when using Google Assistant on your phone, as it doesn’t know what room it is currently in. There are other limitations to deal with, like adding a light to multiple rooms, but can be addressed using SmartThings scenes and Home Assistant groups. To get a better sense of what happens when you say a command, here is my understanding of Google Assistant’s logic when processing light commands:


- **``Turn off the lights``** turns off the lights in the room where the Google Home speaker is located.
- **``Turn off the living room lights``** turns off the lights in the Google room titled “Living Room”, or the light named “living room.”
- **``Turn off all the lights``** turns off all the lights in the home where the Google Home is located.
- **``Turn off the lights upstairs``** will turn off a group of lights titled “Upstairs” or any lights with the word “upstairs” in their name. The group must be defined in Home Assistant or SmartThings (as a scene) if lights in this group are already assigned to rooms in the Google Home app.

### The Problems
Google and Amazon continue to add new features at a rapid pace, making it a futile effort for me to do any detailed comparison between the two. One area where Google lacks is integration with video services like Hulu, Playstation Vue, and Prime Video. Using a Google Home speaker, you can say **``Play Castlevania on Netflix``**, but not **``play The Good Place on Hulu``** on a Chromecast. To my surprise, Amazon Alexa is much better at voice control, supporting deeper voice integration with Netflix, Hulu, Playstation Vue, Prime Video, and other smaller channels. Voice control in media services is not a deal breaker for me since it doesn’t work on most of the apps I use anyways. 



<figure class="align-center">
 <a class="image-link" href="assets\images\other\google-media-integration.png" ><img src="assets\images\other\google-media-integration.png" alt="" /></a>
 <figcaption>
   The list of services that support deeper voice control with Google Assistant and Chromecast.
 </figcaption>
</figure>
After testing Google Assistant with an LG TV, I've learned there is a ~ discrepancy on ~integration between Google Assistant and media devices ~. There is deeper voice integration with more apps using Google Assistant and LG TV, but not with Chromecast. So I can say `play The Good Place on Hulu` and it works on an LG TV. ~. In the Google Home app settings, you can configure the `Default TV` setting for each Google Home speaker, but the LG TV is not available to select.



Google Assistant is directly integrated into the home screen of phones running the latest stock Android, yet my phone still has trouble responding to the **``OK Google``** phrase, even when the phone is charging or on the home screen where Google Assistant is active. I was expecting better integration than this, but I understand phones can’t always be listening. That would be creepy anyway.

Google and Amazon’s voice assistants work best when there is only one user to recognize. Google supports voice matching and multiple accounts, but in practice, I found little success with Google Home differentiating between my roommate and my voice. It is not a problem for controlling lights and TV, but becomes a problem when playing music on Spotify—Google would end up playing music on the wrong Spotify account and Spotify terminates my active music session. I haven’t tested Amazon Echo and Alexa Household feature either, but their multi-user support is limited to two people. Again, this is an annoyance when playing music, but not controlling lights. 


<!-- Product Review section -->
<hr class="minor" />

## The Competition

<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\logo\alexa.png" alt=""/>
        <figcaption></figcaption>
      </figure>
      <h3>Amazon Alexa</h3>
      <p><strong>If you already have Amazon Echo speakers and Fire TVs, then Amazon Alexa is sufficient for basic control of lights, and will likely catch up in feature set with Google eventually.</strong> Alexa is much better at voice control with video services than Google and its Fire 4K TV sticks are of great value, making it an almost perfect pairing for media.  The only missing features I can think of are Youtube (not a big deal), Youtube TV (a bigger deal) and using multi-room audio with your local music library via Plex. I still don’t think it’s worth switching ecosystems if you are already invested in one. There is one feature on newer Amazon Echo devices unique to Alexa, and that is <a href="https://www.tomsguide.com/us/alexa-guard,news-28882.html">Alexa Guard</a>, which can detect the sound of windows breaking from a burglary.</p>

      <p class="box"><i>It was brought to my attention that some Alexa users don't realize key features exist, like <strong>room awareness</strong>. By adding an Echo device to an Alexa group, you can now say <strong>"turn off the lights,"</strong> and Alexa will turn off the lights and light switches in that group. If you create a group that includes the devices in the living room, then Alexa will understand you mean to turn off the living room lights, if you are speaking to the Echo speaker in the living room.</i></p>
    </div>
    <div class="6u$ 12u$(small)">
        <figure class="align-left">
          <img src="assets\images\logo\siri.jpg" alt=""/>
        <figcaption>
    
        </figcaption>
        </figure>
    	<h3>Siri</h3>
    	<p><strong>Siri and Homekit can’t do much more than basic controls of lights, media, and that’s okay because it doesn’t need to do more.</strong> I use a voice assistant mainly to turn on the lights or set a scene, and Siri can do that just fine. Apple deserves credit for pushing privacy as a feature of their products, including Siri. Normally, I wouldn’t recommend Siri for use in any smart home, but now it is possible for Home Assistant to integrate with Homekit (and by association, Siri) to any light, switch, thermostat, lock, garage door, or media player that Home Assistant supports. Device compatibility is no longer an issue in this case.</p>
    </div>
</div>


