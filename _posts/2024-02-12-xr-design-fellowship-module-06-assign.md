---
title: "XR DF Module 06 - Assignment: Unity Bezi Integration"
date: 2024-02-12T17:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
  - Bezi
  - XR Development
  - Unity
toc: true
header:
  video:
    id: 912549054
    provider: vimeo 
gallery-shots:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot01.png
    alt: "Dock Menu"
    title: "Dock Menu"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot02.png
    alt: "Main app layout"
    title: "Main app layout"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot03.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot03.png
    alt: "Switching to edit mode"
    title: "Switching to edit mode"

---

## Module 06 - Unity for prototyping - Turn previous project into an interactive prototype for Meta Quest

![Me actually playing my prototype in Unity]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/06/quest-shot02.png)

You may access the [project's repo here](https://github.com/tiagomms/xrdf-module06-bezishapes-unityIntegration) or you can actually [test the project build by downloading this folder](https://drive.google.com/drive/folders/1GCG6kFadY4lRinV87lTmMSwp0Y0RXqgC?usp=sharing) into your Meta Quest. 

### Project build versions & hardware
- Unity 2022.3.16f1
- Meta XR SDK All-in-one 60.0.0
- Bezi Unity Bridge 0.1.3
- Meta Quest (v2 onwards)

### Challenge

The goal of this assignment was to add interactivity to one of our previous ShapesXR/Bezi prototypes using Meta Quest Building Blocks. 
I choose the Module 01 Bezi's project, because this was my first course project, the idea was simple and it would be a way to review Bezi. Watch the video above to see how it turned out.

To see the original project and explainer, you can access to the [Module 01's project page](../xr-design-fellowship-module-01-post-assignment/) and see its video or actually play with the prototype below made in Bezi.

{% include video id="848531256?h=435fa395d0&dnt=true" provider="vimeo" %}


<div class="responsive-video-container" style="padding-bottom: 500px;">
  <a id="assignment-module" target="_blank" href="https://bezel.it/7ixmko" style="">
    <span class="btn">Bezi prototype full page link</span>
  </a>
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezel.it/7ixmko" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>


Making a Unity prototype as close as possible to my Bezi's prototype turned out to be a bad idea because the Bezi's integration does not send to Unity most animation data nor their order, so I had to invent, manually add data, and code ways to make it work. I became frustrated with the development process, and thought of changing into a ShapesXR integration project. But, I had already started this one. 
Thus, this became my "code-based" prototyping project for Bezi. Here are some of the main things I did:

- Imported [Bezi's project from Module 01](../xr-design-fellowship-module-01-post-assignment/) into unity with Bezi's Unity Bridge package.
- Bezi's imported project did not have the full state and animation data (just position and rotation). However it included data from all events and their separate IDs and to which state they would pass to. So I used this to overwrite Bezi's scripts to include scale, fade In, fade Out and material changes.
  - All properties added in BeziSceneGraph classes: State, Animation, Scale, BeziVector3, MaterialCustomProperties to change the Bezi's material shaders.
- Developed script to deploy Bezi animations based on the Bezi behavior object and Bezi Interaction id's (CustomBeziTriggerAnimation).
- Each time you imported bezi prefab, the bezi unity bridge only provided the current state of your prototype on the website's edit mode. So to test each interaction individually and narrow down the development, I started importing the bezi prefab in each main step: 
  - just having the keyboard ovelay, 
  - then have the dock open and click on the app, 
  - then having the app open and switch between normal and edit mode.
  - In the end, I merged all these interactions into a single Bezi prefab that started when you already had your glasses on and saw the overlay on the keyboard to open/close the dock.

{% include gallery id="gallery-shots" caption="Screenshots of each prototype stage. I would import the bezi prefab for each stage to narrow down the development for each interaction, then merged it all in one." %}

- Develop script to toggle between Bezi animations (open/close dock, open/close app) (ToggleDock - terrible name but didn't change to not lose data in the inspector afterwards)
- Using Meta's building blocks, added the ability to poke, point, pinch, grab. 
  - Added the respective building blocks to make objects interactive (example: open/close dock used a pokeable item building block).
  - Used Meta's Interactable and Pointable Interactable Unity Event Wrapper to trigger sounds, and events on Hover, Select and Unselect.
- Based on Meta's distance grab and snap example scenes, created my own logic to distance grab the app's object and snap it between the App Normal and Edit states - perform this by triggering Unity Actions between changing states.
  - Coded it in a way that I could add more states if the app needed, based on dragging and letting it snap to location


## Issues
### Hardware:
- Only works with Meta Quest. 
- Next stage would be use to Unity XR Framework to expand usage or to Vision Pro with eye tracking

### Technical issues 

**There were a lot of them and that is why it took so long to finish - thus I didn't have time to focus so much on design improvement:**
- Bezi Unity bridge: 
  - is still a beta version - practically all state data is not passed (except position and rotation).
  - The animations are not ready to be deployed, you essentially have very long Lists of state and interaction data in the inspector.
  - Didn't find documentation in how to quickly get the animation that I want at the certain moment. So I had to develop scripts to trigger my main events. But once it worked it was exhilarating.
  - The bridge also assigned the inverted x position values for some unknown reason, so I added a method to do this for me. 

- Meta XR Building Blocks:
  - they are very nice, but there is a fundamental lack of documentation on Meta's scripts and in the examples. 
  - Despite the fact they are very cool to use, to deploy them still requires a Unity developer's knowledge. 

- Meta XR: 
  - The development in Macs is still very painful. Not even the Meta's XR Simulator works there. Had to transition project to my old reliable beasty Windows to test development in play mode.

### Design:
- Grabbing and point/pinch logic works quite well
- Pokeable items are a bit glitchy (then again it is normal for small items due to capturing hand's accurate depth is a hard problem)
- The snapping part is the part that requires some improvements: 
  - I found out dragging the model between states is not as intuitive as I would hope. However if you stop dragging, I coded in a way to move it again to default position after less than a second.
  - I created then 2 snap areas to switch between states so it would be easier to drag the object to desired state. 
  - Probably adding text to them: Edit Mode, Menu Mode would help immensely users


### Feedback

From [Billy Kwok](https://www.linkedin.com/in/billykwokhk/), this month's module expert:

![Very positive feedback from billy on this work]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/06/feedback-module06.png)

### Conclusion

If I knew what I knew today, I would have done the full prototype from ShapesXR because the integration all ready provides each stage. Plus animatino data is way harder then static stages to handle. And I guess the code would have been easier (to go to a shapes prototype next stage, and possibly change view point (through teleport)).
Then again, this project ended up unexpectedly to be a way of reviewing Meta's current SDKs and actually do a prototype from start to finish.
