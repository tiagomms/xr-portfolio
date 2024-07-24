---
title: "XR DF Module 09 - Assignment: Spatial Audio Design Workflows for XR Prototyping"
date: 2024-07-22T17:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
  - Spatial Audio
  - Audacity
  - Atmoky
toc: true
header:
  image: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/live-session.jpeg
gallery-atmoky-dome:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-dome-01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-dome-01.png
    alt: "Atmoky Dome - how it looks like"
    title: "Atmoky Dome - how it looks like"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-dome-02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-dome-02.png
    alt: "Atmoky Dome - main menu"
    title: "Atmoky Dome - main menu"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-dome-03.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-dome-03.png
    alt: "Atmoky Dome - real time attenuation menu"
    title: "Atmoky Dome - real time attenuation menu"
gallery-other-atmoky-demos:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-engage.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-engage.png
    alt: "Atmoky's Engage - Demo Spatial Audio communication tool"
    title: "Atmoky's Engage - Demo Spatial Audio communication tool"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-town.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/atmoky-town.png
    alt: "Atmoky Town - surprisingly accurate sound in 2D world"
    title: "Atmoky Town - surprisingly accurate sound in 2D world"
gallery-audacity:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/audacity-01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/audacity-01.png
    alt: "Audacity Menu - changing the sample amplitude through the envelope tool"
    title: "Audacity Menu - changing the sample amplitude through the envelope tool"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/audacity-02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/09/audacity-02.png
    alt: "Audacity - compression effect to level sample sound (very helpful for looping)"
    title: "Audacity - compression effect to level sample sound (very helpful for looping)"

---

## Module 09 Assignment - Spatial Audio Design Workflows for XR Prototyping


You may access the [looped audio sample I made using Audacity from Michael Jackson's Billie Jean](https://drive.google.com/drive/folders/1oMTdsdz1RJWzeeSYRpKy9I8FCw7pIIM0?usp=sharing) - I do not own any copyrights nor I intend to get remuneration out of the song, this project was just for educational purposes. 


### Tools
- Audacity 
- Atmoky


## Challenge

This month course was mostly theoretical in regards to the importance of spatial audio. 

At the end, we had just a couple of exercises to do:
1. Analysis - identify diegetic, spatial, looped sounds and their opposites from a short gameplay video
2. Prepare a looped sound using Audacity and export it in WAV
3. Analyse demos in Atmoky - company focused on bringing hyper realistic spatial audio into XR, Games and Web

### Challenge 1 - Sound Analysis on a short gameplay 

I chose to do my analysis on a small video gameplay from Spiderman for PS5 (great game btw). 
{% include video id="sR0EkVnDRrk" provider="youtube" %}

There were a lot of sounds to analyse and detect from this small video:

- Diegetic elements (sounds that are intrinsically part of the environment): 
  - city background noise (persistent), 
  - throw web sound [slingshot 0:00, web sling 0:05, web line 0:23], 
  - stretch web after slingshot setup [0:01-0:03, 0:33-0:35], 
  - release web grunt [from slingshot 0:03, 0:36, from web sling 0:05]
  - walking on web line (after each foot is placed) [0:24-0:30]
  - noise from propulsion after web swinging
  - car honking if passing to close while web swinging - 0:05
  - bump on the floor - 0:47

- Non Diegetic elements: 
  - slow motion hum (after pressing button) [0:08-0:11, 0:14-0:18], and releasing [0:11]
  - low background music (persistent - most noticeable at 0:14-0:18 and 0:39-0:47)
  - pirouette sound on performing flips (0:44-0:46)
 
- Looped sounds (that are recurring): slow motion hum sound, background music in city (at some point it repeats), noise from propulsion after web swinging (more intense in amplitude if speed is higher)

- Non Looped sounds (non recurring, occur once and stop): web throw, release web, walking in a web line, car honking, pirouette sound on performing flips (only triggered when playing makes a full stunt thing) 

- Non spatial sounds: background music in the city. It is discussible that the 2 other identified non-diegetic sounds are spatial or not
- Spatial sounds: the rest

### Challenge 2 - Looped sound sample

You may access the [looped audio sample I made using Audacity from Michael Jackson's Billie Jean](https://drive.google.com/drive/folders/1oMTdsdz1RJWzeeSYRpKy9I8FCw7pIIM0?usp=sharing). In the folder you have the Audacity project with all my configurations and the final result in WAV format. 

I used Audacity to :
- select play area (16.395) seconds and retrieve sample
- Used an audio effect called compression to level the sound at all stages in the loop
- Exported project in Stereo wav 16 bit 44.1kHz

{% include gallery id="gallery-audacity" caption="Audacity Configurations" %}

As mentioned previously, I do not own any copyrights nor I intend to get money out of the song/loop. This project was just for me to learn some basic sampling techniques in Audacity. 
You need Audacity to open the file in .aup format (audacity project format)


### Challenge 3 - Play Atmoky demos

[Atmoky](https://atmoky.com/) is a leading expert in making sure Audio is delivered to the users as real as possible. Their website has some really nice demos to showcase spatial audio. To hear the demos you should use some better high-quality headphones.

Below I mention the 3 main demos provided. 

#### Example 01 - [Atmoky Spatial Audio Dome](https://dome.atmoky.com/)

This demo allowed the user to import their own audio samples and control the location and sound attenuation of each sample through a single JSON file (loaded before the experience started). You can also assign colors to the sound orbs for easier identification. 

Additionally, it has an attenuation menu that changes how the sound attenuates in real time.

The sound is just not stereo - it takes into account elevation from audio source. 
Must use headphones to understand the difference. 
Really cool stuff. 

{% include gallery id="gallery-atmoky-dome" caption="Atmoky Dome" %}


#### Example 02 - [Atmoky Engage](https://meet.atmoky.com/)

This demo was not as fun solo. It is a place to test spatial audio between several participants. It also showcases attenuation due to having a virtual wall (like in real life). You can barely hear the sounds triggered from the other side of the wall, unless you increase the reverbation. 


#### Example 03 - [Atmoky Town](https://town.atmoky.com/)

This is a very good demo but the spatial audio is on a 2D plane. My favorite part is to rotate next to the 2 people talking and hear how the sound of the voices propagate from one to the other as I rotate in the middle of them. 

{% include gallery id="gallery-other-atmoky-demos" layout="half" caption="Atmoky other main demos - Engage and Town" %}


## Feedback (coming soon)


### Next Steps 

- Actually use Atmoky spatial tools in Unity (they have a plugin)


## Conclusion

This module was quite thereotical and [Scott](https://www.linkedin.com/in/sclooney/) really had a lot of insight. Unfortunately we didn't have a big project as the other modules, but we learned a lot in terms of how audio is treated for games and XR experiences.

Thank you [Scott Looney](https://www.linkedin.com/in/sclooney/) and the whole XR Bootcamp team for this module! 

