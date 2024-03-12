---
title: "XR DF Module 01 - Spatial Design 101 From 2D to 3D"
date: 2023-07-20T20:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
  - Bezel
toc: true
header:
  image: /assets/images/xr-bootcamp/xr-design-fellowship/module/01/live-session.jpeg

---

Here is a glimpse of what I have learned during Module 01 of the XR Design Fellowship program!

As mentioned in the [intro article](../xr-design-fellowship-begins/), I am mostly paraphrasing experts and centralizing the learnings we get from them and the XR Design Fellowship team. For me this is mostly a learning summary of what I have learned this month.

## Glimpse of our module
This was the first month of XR Bootcamp's XR Design Fellowship program.
Here is XR Bootcamp's glimpse into the module:

* Dive right into spatial design principles, where our expert will untangle complex concepts into easy-to-understand bites.
* Gear up for the visionOS design critique session! Selected community members get to present their work and receive feedback straight from the top.
* The journey continues with a deep-dive into the Design Critique session, focusing on critical elements like Field of View (FOV), Ergonomics, and Depth. This session will cement your understanding of spatial design.
* Feast your eyes as our guest lecturer unveils the Bezel's visionOS Demo. This showcase will give you a glimpse into the cutting-edge creation in XR design.

This month's live session was with the super fun [Daniel Marqusee - XR Designer for Bezi](https://www.linkedin.com/in/daniel-marqusee-6665694b/). We learned a lot from him.


## 01. Pre-assignment

This was our "homework" before the live session with Daniel. 

### 01 - Screen vs Spatial Interactions
![Pre-assignment 01 Question]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/question_screen_spatial.png)
![Pre-assignment 01 Answer]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/answer_screen_spatial.png)

### 02 - Prototyping with Bezel
Essentially, followed these tutorials from Daniel Marqusee: 
* [Create Portal in Bezel with BlockadeLabs Skybox AI Generator](https://www.youtube.com/watch?v=apuJnuLa2SI) - here's [my Bezel portal](https://www.bezel.it/file/10cf145a-4e1e-4c91-bb6d-b352512c7c06) 
* [Bezel Tutorial for State Machine and Timeline](https://www.youtube.com/watch?v=Ep3RmZCGHOI)
* [Bezel AR Prototype in Figma and Bezel from scratch in just 16 minutes](https://www.youtube.com/watch?v=7Y9xGpRM9QY) - to show me how to import Figma panels into Bezel

### 03 - Create your own VisionOS pro draft
Since I never played with these tools before, I wanted to start really small. My goal here was to use Figma as well for the first time. 
* Download the [Apple Design Resources - visionOS for Figma](https://www.figma.com/community/file/1253443272911187215/Apple-Design-Resources---visionOS)
* Understand a bit how both Figma's Apple Design and [Float Grid Template](https://docs.floatgrids.com/getting-started/overview) work
* Added date/time pickers from Apple Design to my Float Grid Template (attempted to mix & match colors using the libraries in place, and change the Float Grid Primary color set) => not used on this draft.
* Import panels from my Figma template to Bezel. Make some animations and buttons.

In the end, I made a very simple prototype:
* Trigger Button - to bring and make the dock disappear, like in Marqusee tutorial.
* In the Dock, used Bezel's edit object functions to make my first "App" logo ( " T " )
* The app opens a template panel from Float Grid Figma template, and a 3D cube (from the T logo to the main space).
* When hovering, the cube rotates. 
* When clicking the cube, the panel goes backward, and the cube takes the main stage. Clicking again, reverts the position. The idea here is to simulate a drag cube to center space. If selected, should take center stage and the panel without disappearing moves a bit behind.
* There is a bug with bezel animation between the hover and clicking states. It is not working well for now.


<div class="responsive-video-container" style="padding-bottom: 500px;">
  <a id="assignment-module" target="_blank" href="https://bezel.it/x29xt3" style="">
    <span class="btn">Bezi prototype full page link</span>
  </a>
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezel.it/x29xt3" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>


{% include video id="845706037?h=80eecad37d&dnt=true" provider="vimeo" %}

## Live Session

![Live Session - From Flat to Spatial]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/01/live-session.jpeg)

[Daniel Marqusee](https://www.youtube.com/c/DanielMarqusee) made a great session and was super helpful with his feedback and insight. Here are a few takes of the session:

* Apple is the first company trying to lay out a blueprint for designing in the XR space and this is really important. They play it safe, but it makes sense because this is a transition period for most people (including designers) not used to XR in general.
* People will try to break the Volume cage Apple created, and get more and more creative to get into full immersion.
* Designers should push for shared spaces with minimal functionalities, and then full space experiences for maximum work. They should be inspired in games (10% UI, the rest are physical affordances).
* Design fields will become intermingled and teams will get bigger.
  * AI will play a very important role with in these teams. They will help build & design for all devices - with the end goal of making the product quickly adaptable to full spaces and accessible for all. 
* Learning 3D Modelling is crucial so that you don't become too dependent on others.
* Learn 3D Content & Depth (don't just follow Apple's examples - understand angles and trigonometry, ergonomics) - Parallax and stereoscopic content will have a come back.
* Don't abuse movement or immersion but find ways to minimize cognitive load while being super helpful.
* Advanced Inputs will expand - Gaze, and Pinching are limited tools for interaction (think of the Apple Pencil for the iPad - it is way more superhuman than the finger) - we need these sort of devices for the spatial space.
* Master the tools you need to get your concepts across 
  * Bezel for XR prototyping with teams that don't have access to devices or Unity
  * ShapesXR for test concepts out in the virtual space
  * Unity for development
* Design with Accessibility in mind will be mandatory in the next years. Accessibility will be for everyone, and from the ground-up. Apple already shares in how to gather head, voice, hand data for these cases - more to come.
* It is normal to have a lot of growing pains in this field - it is something new.

## Post-assignment

After the live session, and seeing some of my colleagues work, I tried my best to upgrade my prototype.
See my other article on the [Module 01 post-assignment and development journey](../xr-design-fellowship-module-01-post-assignment/)

## Sum-up

It was intense but as you might tell, I am learning a lot. 
I am very happy with this opportunity to learn from experts and from my design colleagues. 
It is being a privilege.

## Thoughts of the month

* As designers our role is to first create tools with as little feeling as possible, so they become universal. We should avoid in these prototypes to reduce cognitive load (example: 3D text which is way harder to read and detect patterns than 2D text) - *[Mike Alger](https://www.youtube.com/watch?v=4o__z7aPlMw)*
* Avoid scope creep (by Daniel Marqusee) - really have to work on that one and constrain myself to time schedules.
* As usual, always think how do you want your product to work. It is perfectly normal to feel unsatisfied with your work - it is always an iterative and working process (Daniel Marqusee again, during our live session).

