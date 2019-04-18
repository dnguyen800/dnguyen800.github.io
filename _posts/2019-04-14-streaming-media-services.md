---
layout: page
title: Streaming Media Services
short_title: streaming-media-services
excerpt: Music, TV and movies have never been so accessible as they are today, thanks to streaming media services.
competitors: "Spotify, Plex, Pandora, Youtube Music, Tidal, Apple Music/iTunes, Google Play Music, Amazon Music, Volumio"
permalink: /streaming-media-services
image: assets/images/overlay-ws/music.jpg
image_url: https://unsplash.com/photos/U_z9Y0rEIJc
image_credit: Nadine Shaabana on Unsplash
categories:
    - "Music"
    - "Media"
    - "Home Automation"
---

<!--more-->

# Music

#### I’ve personally tested the following:

|---
| ![](assets\images\logo\spotify.png){:.image.logo} | ![](assets\images\logo\google-play-music.png){:.image.logo} | 
|:-:|:-:|:-:
|  ![](assets\images\logo\plex.png){:.image.logo}   | ![](assets\images\logo\volumio.png){:.image.logo} | ![](assets\images\logo\mopidy.png){:.image.logo}

## What you need to know

Music is a big part of my life, and so I wanted it to be a major feature of my home. I love rummaging through my music collection, checking out the album covers and reading the liner notes. It spurs fond memories of how I discovered the artist, or how I felt when I listened to the album for the first time. With the help of a smart home, I wanted to recreate that nostalgic feeling in a digital form somehow, and have music playback be an integrated and seamless experience. It should be easy to find a song on any platform (phone, laptop, voice) and play on the speakers in the house. 

I love the current state of streaming music services—I can access music discographies from thousands of artists, and get music recommendations tailored to my listening habits. Although I no longer have any interesting recent memories of discovering music, I’ve been able to find so many new artists that I never would have found if I continued manually searching for music the old way. 

I do want to acknowledge my music listening past (including the good and bad artists) by having my CD and MP3 collection available to play on the speakers, so it was important to find a solution that can play both streaming and local music on my Chromecast built-in speakers. Luckily, those solutions exist now and are fantastic to use.

### Considerations before purchasing a music subscription

<ul class="alt">
  <li>Most subscriptions offer a family plan that you can split among your household members. </li>
</ul>


### What you get with a music subscription

<ul class="alt">
  <li>A huge collection of music accessible through a mobile app, web browser, and voice control.</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li>Home Assistant <a href="https://www.home-assistant.io/components/spotify/">Spotify</a> and <a href="https://www.home-assistant.io/components/plex/">Plex</a> components</li>
  <li>Plex does not support <a href="https://forums.plex.tv/t/plex-stream-to-amazon-echo-groups-multiple-echo-devices-at-once/339113">multi-room audio</a> with Amazon Echo.</li>
  <li>Following the steps of the <a href="https://arstechnica.com/gadgets/2017/12/amazon-music-ends-mp3-upload-support-will-end-music-storage-service-in-2019/">Amazon Music shutdown</a>, Google Play Music will be <a href="https://arstechnica.com/gadgets/2018/05/youtube-music-will-replace-google-play-music-but-wont-kill-user-uploads/">shutting down</a> and replaced by Youtube Music.</li>
  <li>Plex Media Server <a href="https://community.home-assistant.io/t/community-hass-io-add-on-plex-media-server/54383">hass.io addon</a> if you want to run the server on a Raspberry Pi with Home Assistant. There are storage limitations as you cannot connect external devices to Hass.io.</li>
  <li>Phlex <a href="https://community.home-assistant.io/t/community-hass-io-add-on-phlex/70378">Hass.io addon</a> adds Google Assistant capabilities to Plex. Requires the <a href="https://github.com/d8ahazard/Cast.bundle">Cast.bundle</a> Plex addon to be installed.</li>
  <li><a href="https://forums.plex.tv/t/how-to-request-a-x-plex-token-token-for-your-app/84551">How to generate a temporary token for Plex.</a></li>
  <li>Amazon Fire TVs can watch Youtube through unofficial apps like <a href="https://smartyoutubetv.github.io/">Smart Youtube</a>.</li>
</ul>

<!-- Product Review section -->
<hr class="minor" />

![](assets\images\logo\spotify.png){:.image.dan-left}

## Spotify

**For streaming music, Spotify is, without a doubt, the best offering not only for its catalog of music but because it is the most openly supported music platform out there.** Spotify works with voice assistants, web browsers, Android, iOS, and Amazon platforms—not many music services can make that claim.  Even open-source platforms like Home Assistant and Volumio can access the Spotify API to control playback like the official app.  For the music lover, the playlist curation and personalized music recommendations are so precise that Spotify can find a song I love from an artist or album I don’t like. 

<figure class="align-center">
 <img src="assets\images\other\spotify-desktop.jpg" />
 <figcaption>
A view of the Spotify desktop app for Windows.
 </figcaption>
</figure>

Spotify supports all major multi-room audio formats: Chromecast Built-in, Amazon Echo, Sonos and Apple Airplay 2. Audio quality is respectable, using 320kbps Ogg Vorbis format (as long as the **High Quality Streaming** setting is enabled). That is the best quality you can get before going for lossless audio like FLAC, or Tidal’s lossless music service. 

### The Problems

There are a few areas that Spotify falters: one is the lack of unofficial remixes and live sets that are somehow allowed on Youtube. The Spotify Windows app and Home Assistant cannot cast music to Chromecast speakers directly. You will need to use the mobile app, a voice assistant or web browser to do that. Amazon Echo and other speakers supporting Spotify Connect work, so this is likely an inherent limitation of Chromecast.

### Installation and Smart Home Integration

Spotify is fully controllable in Home Assistant, though selecting a speaker source doesn’t work. I haven’t found a way to play Spotify to a Chromecast speaker using Home Assistant.

Voice control works really well. I can ask to play a particular song, artist or one of my custom playlists.

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/spotify-ha.png" />
        <figcaption>
          <strong>Home Assistant: Good</strong><br>Several steps requiring developer account, edit config file, browser authorization.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Great</strong><br>Spotify works perfectly with Google Assistant.
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
       <img src="assets/images/integrations/spotify-app.png"  />
       <figcaption>
         <strong>Spotify App: Great</strong><br>Amazing!
       </figcaption>
      </figure>
	</div>
</div>


<!-- Product Review section -->
<hr class="minor" />

![](assets\images\logo\plex.png){:.image.dan-left}

## Plex

**For local music, Plex is the best (and free!) app that can organize your music collection and offers the same functionality as popular music apps like Spotify.**  Plex is accessible on web browsers, Xbox One, Playstation 4, Android, iOS, and Amazon platforms, and even remote access to your music isn’t too hard to set up. Chromecast multi-room audio is supported with Plex, but unfortunately, Amazon, Sonos  and Apple’s multi-room audio solutions do not work yet. It sounds like I’m describing Spotify as Plex comes close to providing the same user-friendly experience, which is important to making music playback as easy as possible.

You will be surprised how hard it is to get a Spotify-like music experience for your local music. I tried open-source music players like Volumio, Mopidy, and PiMusicbox, but those tend to miss critical features—like a good search function or artist biographies—that keep it as a bare-bones app. It is amazing how the underlying parts (media scrapers, search, file support) of Plex work together to make a cohesive experience.

<figure class="align-center">
 <img src="assets\images\other\plex-app02.jpg" alt="" />
 <figcaption>
Artist biographies in Plex. It’s fun to read about your favorite artists. Plex also shows similar artists, popular tracks—just like Spotify.
 </figcaption>
</figure>

<p class="box">
<i><strong>Here’s a tip on bypassing Plex Pass restriction when watching videos and music on the phone:</strong> normally, the Plex iOS and Android apps are time-restricted one minute without Plex Pass, but if you play the video or song to a Chromecast, the time limit is ignored.</i></p>

### The Problems

You will need a server or device running 24/7 to run the Plex Media Server. An Nvidia Shield TV or a spare laptop running Windows, Mac, or Linux make for excellent Plex servers. It’s possible to run Plex Media Server on a Raspberry Pi as a [Hass.io add-on](https://community.home-assistant.io/t/community-hass-io-add-on-plex-media-server/54383), but due to the restrictions of Hass.io and Docker, you can only store music on the SD card where Home Assistant is stored. I’m sure there is a way to connect a USB drive, but I’m not familiar with Docker to do so.

### Installation and Smart Home Integration

Music players don’t integrate with SmartThings—that’s expected by now. Home Assistant integrates with Plex but requires an authentication token to connect. I recommend using the temporary token outlined [here](https://forums.plex.tv/t/how-to-request-a-x-plex-token-token-for-your-app/84551) and see if that works for your needs. I don't use the Plex component since my Chromecast speakers can control playback, and Home Assistant integrates easily with Chromecast. After getting the token, any device running the Plex app is treated as a media player in Home Assistant.

Voice control is more difficult to get working on Google Assistant, though I think Amazon Alexa has an official integration with Plex. Getting Assistant to work requires installing a Hass.io add-on called [Phlex](https://github.com/hassio-addons/addon-phlex/blob/v1.0.0/README.md) and [Cast.bundle](https://github.com/d8ahazard/Cast.bundle). It would take some time to install and test it, so I couldn't do it at the time of this writing.

<figure class="align-center">
 <img src="assets\images\other\jriver-app.jpg" alt="" />
 <figcaption>
Jriver Media Center has an extensible set of tools to clean up metadata and cover art.
 </figcaption>
</figure>

Before using Plex, I recommend cleaning up your music collection first. That means converting CDs to the FLAC lossless format, fixing any low-resolution cover art, standardizing artist and album names, fixing track numbers, and renaming files and folders. It’s a one-time effort to do over the weekend, but worth it to see the result—an immaculate, organized collection that is fun to browse through. I used Jriver Media Center to handle the CD ripping, metadata scraping, and file/folder renaming. A free 30-day trial is available, which should be enough time to perform the cleanup.


<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/plex-ha.png" />
        <figcaption>
          <strong>Home Assistant: Difficult</strong><br>Requires obtaining a temp token. Cover art doesn’t load.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
         <strong>Voice: Difficult</strong><br>Requires Phlex and Cast.bundle add-ons to work with Google Assistant. Must expose HAinstance to the internet.
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
       <img src="assets/images/integrations/plex-app.png"  />
       <figcaption>
         <strong>Plex App: Great</strong><br> Simple, and easy-to-use.
       </figcaption>
      </figure>
	</div>
</div>

<!-- Product Review section -->
<hr class="minor" />

## The Competition


<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\logo\google-play-music.png" alt=""/>
        <figcaption></figcaption>
      </figure>
      <h3>Google Play Music</h3>
      <p>Google Play Music was my alternate method of playing my local music collection, but unfortunately it will be <a href="https://arstechnica.com/gadgets/2018/05/youtube-music-will-replace-google-play-music-but-wont-kill-user-uploads/">replaced by Youtube Music</a>. It's not technically playing music locally, as I first needed to upload my 80-gigabyte music collection to Google's servers and sync it thereafter. A Google Play agent application exists to monitor folders and upload new tracks. </p>

<p>The Google Play Music mobile app works, though navigation is annoying as the app is constantly pointing you towards radio stations and some form of paid music subscription.</p>

<p>There are limitations on the number of times you can download your entire collection and the number of devices you can stream your music from. Google is also replacing Google Play Music with Youtube Music, so it's likely the music storage option will go away as well. Amazon Music also canceled its local music service in 2019 so there aren't many options left besides local storage.</p>
   </div>
   <div class="6u$ 12u$(small)">
        <figure class="align-left">
          <img src="assets\images\logo\volumio.png" alt=""/>
        <figcaption>

        </figcaption>
        </figure>
    	<h3>Volumio</h3>
    	<p>Volumio is a well polished, open-source music player with a big emphasis onHi-Fi audio, but lacks convenient features I needed. It is easy to flash a Volumio image onto an SD card. The default skin is very nice, and there's a Spotify plugin available to access Spotify music and local music in one interface. Chromecast support isn't available, though not impossible if someone were to create a plug-in.</p>

<p>Volumio's navigation is pretty basic. There aren't any artist biographies, related music or artists -- it's not that fun to browse through music in Volumio as it only displays artist, album, and song names. At least a Volumio mobile app exists and looks professional. Home Assistant integration with Volumio exists and works well, though I'm not sure if the album cover art displays in Home Assistant.</p>

<p>Volumio didn't fit my needs, but I still think it's a solid application that might be useful for others who want a high fidelity music solution in their smart home.</p>
    </div>
    <div class="6u$ 12u$(small)">
        <figure class="align-left">
          <img src="assets\images\logo\mopidy.png" alt=""/>
        <figcaption>
          
        </figcaption>
        </figure>
    	<h3>Mopidy</h3>
    	<p>I used Mopidy for some time before realizing Plex does everything I needed, but better. Out-of-the-box, Mopidy looks barebones but after adding the <a href="https://github.com/mopidy/mopidy-spotify">Spotify plugin</a> and the <a href="https://github.com/jaedb/Iris">Iris theme</a>, it looks like a professional music player.</p>

<p>There is a way to stream from Mopidy to Chromecast speakers, but the method I used added a 5-second delay before playback, reduced sound quality, and issues skipping songs, or playing a new song. Basically, Mopidy is streaming live audio output to an Ogg Vorbis file, and you send the URL of the file to the Chromecast to play. I followed a <a href="https://www.vittoriomonaco.de/home-automation-part-7.html">tutorial</a> by Vittorio Monaco to figure this out.</p>

<p>For some reason, I never got the music to play through my web browser. It annoyed the heck out of me and made me give up on the platform.</p>
   </div>
</div>

<!-- Product Review section -->
<hr class="major" />

# Live TV Providers

**Competitors in this space:** Youtube TV, Playstation Vue, Hulu Live, Sling TV, Philo, OTA local channels

#### I’ve personally  tested the following:

|---
| ![](assets\images\logo\youtubetv.png){:.image.logo}  | ![](assets\images\logo\slingtv.png){:.image.logo} | ![](assets\images\logo\hdhomerun.png){:.image.logo} 
|:-:|:-:|:-:
| | |

## What you need to know

If you came here hoping for a way to integrate your Xfinity, Verizon, or Dish Network TV receivers with Home Assistant or Amazon Alexa, then you’re out of luck! Those are closed ecosystems and you’re stuck with whatever features they offer. To be fair, the Xfinity app has improved and the Xfinity remote’s voice feature worked well during the times I tried it. If you absolutely refuse to cut the cord with cable TV, then the Logitech Harmony remote can add some voice control and Home Assistant integration but requires a lot of testing to get it right. To be honest, I haven’t found a reason to use my voice to watch live TV and prefer using a remote to browse through the TV guide or recordings. So you’re not missing much by not integrating.

There are a growing number of video streaming services that offer live local TV and select premium channels for a lower price and no contracts. These integrate services better with voice assistants and Home Assistant by association of the Rokus, Chromecasts and Fire TVs it supports. So let's review one of these services!

### Considerations Before Purchasing an Internet TV Subscription

<ul class="alt">
  <li><strong>Do you really need another subscription that you may not use?</strong> Consider subscribing and canceling when your TV show’s season is over.</li>
  <li><strong>Check your internet provider’s internet speed and bandwidth caps.</strong> Your TV watching habits may disrupt another’s video gaming session or exceed bandwidth caps.</li>
</ul>

### What You Get With an Internet TV Subscription

<ul class="alt">
  <li><strong>With Youtube TV, share the subscription with five others in your Google Family.</strong> You can only change families once a year, and can’t be in more than one family. Geographic restrictions also apply, though in my testing, the Bay Area region is fine.</li>
  <li><strong>Watch TV on the go with your phone, even when traveling across states.</strong> Eventually, these apps block local TV access if it detects you’ve been living in a different area for months.</li>
</ul>

### Recommended Reading

<ul class="alt">
  <li>Youtube TV <a href="https://tv.youtube.com">official site</a></li>
  <li> Using Google Assistant on <a href="https://support.google.com/youtubetv/answer/7529864?hl=en">Youtube TV with Chromecast</a></li>
  <li>Share Youtube TV membership with your <a href="https://support.google.com/families/answer/7251139?hl=en">family group</a>, up to 5 people.</li>
</ul>

<!-- Product Review section -->
<hr class="minor" />

![](assets\images\logo\youtubetv.png){:.image.dan-left} 

## Youtube TV

**I've been using Youtube TV for months and it provides a solid TV viewing experience as well as some useful smart home features, like advanced voice control with Google Assistant.**  Like any good streaming service, Youtube TV supports playback on web browsers, Chromecast, Roku, Apple TV, and most new TVs (2016 models or later). Streaming starts within seconds without any noticeable lag or dropouts, even when watching live sports (which plays at 60fps). The experience convinced me that streaming live TV doesn’t have to suck, unlike my experience with Sling TV.

Voice commands with Google Assistant work really well on Youtube TV (naturally), but only when using Chromecast. Saying “play the latest episode of Conan” works as expected on my Chromecast Ultra, but not on Roku. The most I can do with my voice is to say “open Youtube TV on Roku,” which is not all that useful.

<p class="box">
<strong>Did you know...</strong><br>
<i>Youtube TV also has a generous family sharing option, allowing up to five additional members to have their own Youtube TV account, with three simultaneous streams each. There are certain limitations, like members can switch families only once a year, you can’t join more than one family. and members should be within a geographic range (unconfirmed as to the range).</i></p>

<figure class="align-center">
 <img src="assets\images\other\youtube-tv.png" alt="" />
 <figcaption>
 The Youtube TV app on Android.
 </figcaption>
</figure>

### The Problems

There are some annoyances worth noting before signing up for Youtube TV. Sadly, due to the feud between Google and Amazon, Youtube TV does not work with Amazon Fire TV or tablets. Unofficial installation methods exist (like <a href="https://smartyoutubetv.github.io/">Smart Youtube TV</a>) but are likely to stop working in a few months whenever an app update is required. 

Secondly, finding and favoriting TV shows should be easy, but the app separates on-demand and broadcast shows, meaning you can’t browse through all of FX’s catalog in one spot. In some cases, I had to search for specific TV shows, like TBS’ Miracle Workers, in order to record them. I’m not able to bookmark Mr. Robot either, at least not until after the season premiere occurs. I also noticed the selection of episodes available on demand fluctuates, much to my annoyance. Shows like **Angie Tribeca** on TBS  tends to flip between the first and second half of the latest season every few weeks.

### Installation and Smart Home Integration

<div class="row">
	<!-- Break -->
	<div class="6u 12u$(medium)">
	  <figure class="fourthtest">
        <img src="assets/images/integrations/youtubetv-ha.png"  />
        <figcaption>
          <strong>Home Assistant: None</strong><br>The media streaming device used (Roku, Chromecast) provides basic media playback controls for Youtube TV.
        </figcaption>
      </figure>
	</div>
	<div class="6u 12u$(medium)">
      <figure class="fourthtest">
       <img src="assets/images/integrations/google-home.png" />
       <figcaption>
          <strong>Voice: Good</strong><br>Supports deep integration if using a Chromecast and Google Assistant. Not so good with Roku and Google Assistant.
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
       <img src="assets/images/integrations/youtubetv-app.png" />
       <figcaption>
         <strong>Youtube TV App: Great</strong><br> Simple, and easy-to-use.
       </figcaption>
      </figure>
	</div>
</div>


<!-- Product Review section -->
<hr class="minor" />

## The Competition

<div class="row">
    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\logo\hdhomerun.png" alt=""/>
        <figcaption></figcaption>
      </figure>
      <h3>HD Homerun</h3>
      <p>I bought and tested an HDHomerun Connect tuner and it was a good experience overall, but I've learned that I do not watch live television, besides sports games. With the additional cost for DVR features ($40 annual Plex Pass and available USB hard drive), I decided to go with Youtube TV instead.</p>

      <p>I always had trouble detecting TV channels using my small flat antenna, but the HDHomerun has the best tuner for antennas, in my experience. I used a small flat antenna, mounted it on the wall in the second floor, and the HDHomerun picked up every channel, even the distant ones from 50 miles away. In my 10+ years of fiddling with antennas, I have never been able to get all major TV channels with a small antenna, except with HDHomerun.</p>
      
      <p>The HDHomerun mobile apps are pretty barebones, but it works. There is even an app for the Xbox One that works. Can't see TV guide listing, just live TV. Plex TV works well and the TV guide is much easier to browse, but it takes a few more seconds to load and start watching TV. </p>

<h3>The problems</h3>
<p>The HDHomerun requires a wired connection to the router, which limits where you can place the device and the connected antenna. You cannot cast live TV from Plex to a Chromecast, which was something I needed in my solution.</p>
   </div>

    <div class="6u 12u$(small)">
      <figure class="align-left">
          <img src="assets\images\logo\slingtv.png" alt=""/>
        <figcaption></figcaption>
      </figure>
      <h3>Sling TV</h3>
      <p>I tested Sling TV and made an effort to migrate to it years ago but decided it wasn't worth the money. I couldn't rely on it to stream live sports games reliably, as the video stream would time out or have buffering issues. The lack of DVR and poor on-demand selection made it easy to say no to Sling TV. I don't think the service is much better now, from the comments I read on Slickdeals and the FireTV subreddit.</p>
   </div>
</div>

