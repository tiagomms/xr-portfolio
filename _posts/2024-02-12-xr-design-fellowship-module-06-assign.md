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

You may access the [project's repo here](https://github.com/tiagomms/xrdf-module06-bezishapes-unityIntegration) or you can actually test the [project build by downloading this folder](https://drive.google.com/drive/folders/1GCG6kFadY4lRinV87lTmMSwp0Y0RXqgC?usp=sharing) into your Meta Quest. 

### Project build versions & hardware
- Unity 2022.3.16f1
- Meta XR SDK All-in-one 60.0.0
- Bezi Unity Bridge 0.1.3
- Meta Quest

### Challenge

The goal of this assignment was to add interactivity to one of our previous ShapesXR/Bezi prototypes using Meta Quest Building Blocks. 
I choose the Module 01 Bezi's project, because I thought it would be the simplest one. You can see the video how it turned out.

You can access to the [Module 01's project](../xr-design-fellowship-module-01-post-assignment/) or see the video and actually play with bezi prototype below.

{% include video id="848531256?h=435fa395d0&dnt=true" provider="vimeo" %}

<div class="responsive-video-container">
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezel.it/x29xt3" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>


Since Bezi's is all about interactions and animations it turned out a bad idea, but when I realized that too late so I continued working it out. 
In the end, it became a "code-based" prototyping project. Here are some of the main things I did:

- Imported [Bezi's project from Module 01](../xr-design-fellowship-module-01-post-assignment/) into unity with Bezi's Unity Bridge package.
- Bezi's imported project did not have the full state and animation data (just position and rotation). Had to overwrite Bezi's scripts to include scale, fade In, fade Out, material changes
  - All properties added in BeziSceneGraph classes: State, Animation, Scale, BeziVector3, MaterialCustomProperties to change the Bezi's material shaders).
- Developed script to deploy Bezi animations based on the Bezi behavior object and Bezi Interaction id's (CustomBeziTriggerAnimation).
- Develop script to toggle between Bezi animations (open/close dock, open/close app) (ToggleDock - terrible name but didn't change to not lose data in the inspector afterwards)
- Using Meta's building blocks, added the ability to poke, point, pinch, grab. 
  - Added the respective building blocks to make objects interactive (example: open/close dock used a pokeable item building block).
  - Used Meta's Interactable and Pointable Interactable Unity Event Wrapper to trigger sounds, and events on Hover, Select and Unselect.
- Based on Meta's distance grab and snap example scenes, created my own logic to distance grab the app's object and snap it between the App Normal and Edit states - perform this by triggering Unity Actions between changing states.
  - I coded in a way that I could add more states if the app needed, based on dragging and letting it snap to location

{% include gallery id="gallery-shots" caption="Screenshots of the actual in game experience" %}

### Issues
- Hardware:
  - Only works with Meta Quest. 
  - Next stage would be use to Unity XR Framework to expand usage or Vision Pro

- Technical issues (the biggest ones and that is why it took so long to finish, and didn't have time to focus so much on design improvement):

  - Bezi Unity bridge: 
    - is still a beta version - practically all state data is not passed (except position and rotation).
    - The animations are not ready to be deployed, you essentially have very long Lists of state and interaction data in the inspector.
    - Didn't find documentation in how to quickly get the animation that I want at the certain moment. So I had to develop scripts to trigger my main events. But once it worked it was exhilarating.
    - The bridge also assigned the inverted x position values for some unknown reason. 

  - Meta XR Building Blocks:
    - they are very nice, but there is a fundamental lack of documentation on Meta's scripts and in the examples. 
    - Despite the fact they are very cool to use, to deploy them still requires a Unity developer's knowledge. 

  - Meta XR: 
    - The development in Macs is still very painful. Not even the Meta's XR Simulator works there. Had to transition project to my old reliable beasty Windows.

- Design:
  - Grabbing and point/pinch logic works quite well
  - Pokeable items are bit glitchy
  - The snapping part is the part that requires some improvements: 
    - I found out dragging the model between states is not as intuitive as I would hope. However if you stop dragging, I coded in a way to move it again to default position after less than a second.
    - I created then 2 snap areas to switch between states so it would be easier to drag the object to desired state. 
    - Probably adding text to them: Edit Mode, Menu Mode would help immensely users

### Feedback

(coming soon)


