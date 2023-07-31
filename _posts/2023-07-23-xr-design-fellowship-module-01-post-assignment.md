---
title: "XR DF Module 01 - Post Assignment"
date: 2023-07-23T20:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
toc: true
header:
  video:
    id: 848531256?h=435fa395d0&dnt=true
    provider: vimeo 

---

Here's the assignment of module 01 after the live session with [Daniel Marqusee](https://www.youtube.com/c/DanielMarqusee).

## 01. Post‐Assignment: Vision Pro Prototype ‐ Keyboard Interaction and Simple App

This low-fidelity prototype aimed to display 2 things: 
* a use case of connecting a keyboard to vision OS in which both in sync offer a richer set of possibilities. 
* a use case of a possible app in which is possible to handle 3D models.

The prototype was done in Bezel to showcase a future development. This was the first project for the XR Design Fellowship course, provided by XR Bootcamp, and lectured by [Daniel Marqusee](https://www.youtube.com/c/DanielMarqusee), Bezel's UX, UI and XR designer.

[Prototype Link](https://www.bezel.it/play/096d51bb-edee-418e-863b-a0cef3b7ba68)

<div class="responsive-video-container">
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezel.it/7ixmko" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>

## Specifications
### Responsibilities
Product Design

### Tools
- Figma
- Bezel

### Timeline
12 hours

### Team Size
Just me

## The problem
External devices to Vision Pro will definitely play a roll in supporting Vision Pro remarkable features. [Daniel Marqusee](https://www.youtube.com/c/DanielMarqusee) stated gaze & pinch as sources of input are quite limited. For more complex, personalized and actually enriching experiences other devices (e.g: controllers, keyboards, and new stuff) will definitively play a roll in how Vision Pro will help us shift toward a more accessible and personalized human-computer experience. The goal of the project was an initial thinking experiment in how to combine a vision pro and a keyboard, in which animations and depth will play a major role. 

In addition, I tried to replicate a similar UX in MacOS when opening/closing an app (T icon) - with a few differences considering the role of depth in apps for the Vision Pro. With depth, apps can have modals and menus being displayed according to their importance. In this case, I tested pushing the main menu back when something else is prioritised, but it never disappears totally of line of sight as a reminder.   

### Project Goals
The first main goal was to learn how to use Figma and Bezel, I had no experience working with these tools. As part of the XR Design Fellowship program this first month was to learn prototyping for XR, taking into account Apple Vision, Meta and Google guidelines in how to develop XR experiences. I pretty much followed Daniel Marqusee tutorials until I started playing and delved into something of my own. After tinkering a bit with bezel, this was my vision.

### Project Vision
You can see the video above or play with the prototype above. Here's a brief step-by-step of the prototype.

Someone puts his vision pro glasses on. 
![desk with vision pro]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/PostAssignment-1_5-01.png)

Instantly, the keyboard keys have a layer on top of them for additional interactivity. I can call the dock and get into my app.
![keyboard button with green overlaying button made by vision os]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/PostAssignment-1_5-02.png)

The app main menu is in focus, on the right - the model I was working on previously. 
![app main menu]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/PostAssignment-1_5-03.png)

When I gaze (hover) the model signals me if I want to get back to work.
![gazing model on the right - animation triggers]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/PostAssignment-1_5-04.png)

The main menu and its instructions are sent to the background. 
Now I can work on my model, and an options panel appears right next to it for further customisation.
![Model becomes your main focus. main menu pushed to the background and settings menu appear on the side of the model you are just editing]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/PostAssignment-1_5-05.png)

The project is incomplete and the UX not polished - but for the time I had, I am actually pleased with the result.

![App interaction](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/e14e2dcc-f86d-4da1-ac3f-b6c69e3431c9.gif?ClientID=vimeo-core-prod&Date=1690325439&Signature=306650a85608e2fa8a1c2c5e4129303363199170)

## Development Journey

1. I tried to replicate some UX Apple animations: show/hide dock thanks to a button, maximize/minimize app. 
2. Began developing a simple app (T icon app), in which we should be able to drag a 3D model to the center for further customization, or slide to the left to go back to the main menu. The main app menu is pushed to the back when the 3D model is in the center.
3. The app is independent from the dock. I can hide the dock and still play the app.
4. The UI menus are completely default from Figma's Floatgrids design template. I just changed the primary palette color. Imported them to Bezel.
5. Delivered my pre-assignment as the bezel prototype below. Check out the overall 1st month experience on the course - [link](https://github.com/tiagomms/XR-Bootcamp-XR-DesignFellowship/wiki/01.-Spatial-Design-101-From-2D-to-3D).

<div class="responsive-video-container">
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezel.it/x29xt3" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>

{% include video id="845706037?h=80eecad37d&dnt=true" provider="vimeo" %}

6. Began improving the app animations. I settled on using a third state to avoid the hover/click animation bug I was having (check the challenges where I delve more into this).
7. I began thinking of devices that we may still use in the future, so I added the keyboard. Ideally (if it doesn't cause too much friction) Vision OS macros will overlay the actual keyboard. Light cues should appear when physically touching the keyboard keys. The reason I didn't add a laptop was I think Vision OS in the next years may replace the need for laptops - unless very intensive applications, which require extra processing power.
8. Added a free low-poly VR headset to simulate the experience of putting a headset and seeing a button popping on the keyboard. This button will open/close the dock.
9. (not as I hoped for) Couldn't recreate Apple's glassy effect when tabs are on the background. To compensate, I animated the panel material in bezel - reduced its light transmission and made it darker.
10. (not concluded) Ideally, the dock would show which apps are currently open thanks to the dot symbol on the bottom. I didn't have time to implement a close & minimize button for the app. Right now, clicking on the dock app icon will "open and close" the app. But in the future, clicking should open/minimize, or just toggle and select from all app windows (another great topic to think about!).
11. (not concluded) Began adding signifiers as an app tutorial. The yellow signifier should mean to drag the cube around that center area to then start editing it. Probably a small text screen on top saying that should be nice (that or the actual UI menus make some kind of sense).
12. Added a secondary camera just to show from an external perspective to show what is going on. 


![Secondary camera - Third Person view]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/PostAssignment-1_5-06-SecondaryCamera.png)

## Challenges
### Exploration Time vs System's Design Idea (Scope creep)
Since I didn't have an idea of how I should prototype to Vision OS, I followed Daniel's tutorials and played with Bezel. I probably explored more than focused on specific design principles and overall idea I wanted to convey.

I tried to focus as much as I could to signify what people should click and interact with on this prototype.
As I get more knowledgeable on the topic, I will probably focus more on the idea of what I want to do first. Then perform interviews and A/B testing to really nail down the XR overall UI/UX experience. Otherwise, I will start to fall on what Daniel calls "scope creep", just like I did now.
In the next months, I will definitively try to constrain myself a bit, as UI/UX design is not my background. Hopefully, I get the chance to play a bit with Figma. This month goal was to learn more bezel, and I think I did a good job in that regard. 

### Bezel Limitations
We can't add conditionals to animations on Bezel. I had some conflicting issues between hover and click interactions because of that. To make it kind of work I either reduced the animations duration, or had to add a middle step between these interactions. Unfortunately, sometimes bugs occur despite attempts otherwise. Restart bezel play if needed.

{% include video id="846369287?h=0fa79ee36e&dnt=true" provider="###vimeo-not-used" %}

![GIF - bug conflict between hover and click state](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/1287a840-12a1-4d54-824e-7967a6fc8e3a.gif?ClientID=vimeo-core-prod&Date=1690325353&Signature=24e1bc40eb06af0da56632ba08be489d3493edd7)

## Next steps

* Ideally, I would test in an XR device my Bezel prototype. I tried to follow Apple's and Google's ARCode recommendations of having menus between 1-1.5m away for better readability and interactiveness. The rotation angles for the dock and panels may be a bit off.
* Work more the points 9, 10 and 11 in the development journey.
* Should probably use Figma to blur the app's main menu when the model takes center stage. 
* As my course colleague [Brian C McDonald](https://www.briancmcdonald.com) mentioned 

![Brian opinion on the prototype]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/brian-opinion.png)


### Afterthoughts - on connecting an external keyboard to Vision OS

The idea here is like there are macros in keyboards for pretty much everything, there can be macros specifically for Vision Pro. Probably, opening the apple dock will consist of pinching thumb and index for some seconds while your palm is facing you (like in Meta). But a keyboard connected to Vision Pro may just be a button click.
For selecting and transforming 3D models things, we will probably use gaze & pinch. Coding for more complex immersions, keyboard is probably still the best alternative. For more complex 3D modelling, a mix of keyboard macros to lock, and then gaze & pinch may do the trick (like erasing vertex).
Even though the Vision Pro could actually provide light cues based on the eye getting closer to the keyboard (like the Quest), this may be not a good idea because of some calibration or the keyboard visual cue gaps are too small (Apple recommends a 6px gap between buttons, and the keyboard keys may be too close to each other). 

These features definitely require a lot of user testing and research.


