---
title: "XR DF Module 07 - Assignment: 3D Asset Pipeline for XR Design"
date: 2024-03-04T17:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
  - Blender
  - Bezi
  - XR Development
  - Unity
toc: true
header:
  video:
    id: 919653214
    provider: vimeo 
gallery-sketchfab:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/sketchfab-buddha-wireframe.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/sketchfab-buddha-wireframe.png
    alt: "Buddha model topology and wireframe"
    title: "Buddha model topology and wireframe"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/sketchfab-normal-maps.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/sketchfab-normal-maps.png
    alt: "Rendering of normal maps for added realism"
    title: "Rendering of normal maps for added realism"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/sketchfab-models.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/sketchfab-models.png
    alt: "Sketchfab initial asset selection and notes of things performed in blender"
    title: "Sketchfab initial asset selection and notes of things performed in blender"
gallery-blender:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-buddha-decimate-pivot-point.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-buddha-decimate-pivot-point.png
    alt: "Buddha model decimate and pivot point change"
    title: "Buddha model decimate and pivot point change"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-incense-pivot-point-deleted-holder.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-incense-pivot-point-deleted-holder.png
    alt: "Incense deleted its holder, changed incense rotation and pivot point to non-burning tip"
    title: "Incense deleted its holder, changed incense rotation and pivot point to non-burning tip"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-meditation-bowl-split01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-meditation-bowl-split01.png
    alt: "Split meditation bowl from its stick - just the meditation bowl"
    title: "Split meditation bowl from its stick - just the meditation bowl"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-meditation-bowl-split02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/blender-meditation-bowl-split02.png
    alt: "Split meditation bowl from its stick - just the stick (with rotation and position change); also animation ignored"
    title: "Split meditation bowl from its stick - just the stick (with rotation and position change); also animation ignored"
gallery-shots:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/quest-shot01.JPG
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/quest-shot01.JPG
    alt: "Starting point"
    title: "Starting point"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/quest-shot02.JPG
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/quest-shot02.JPG
    alt: "Meditation mode once incense has been moved"
    title: "Meditation mode once incense has been moved"

---

## Module 07 Assignment - Turn my room into a meditation center


{% include gallery id="gallery-shots" layout="half" caption="Screenshots of playing the prototype in Unity" %}

You may access the [project's repo here](https://github.com/tiagomms/xrdf-module06-bezishapes-unityIntegration) or you can actually [test the project build by downloading this folder](https://drive.google.com/drive/folders/1NxvkJMxLp5KyMjOVTRlYb42K0vj-_kBh?usp=share_link) into your Meta Quest. And you can check out tryout the early bezi prototype here.

{% include video id="919694261?h=910ddc48e7" provider="vimeo" %}

***Attention: to trigger the incense animation you have to click on it, but since it is quite a small object - it is a bit hard.***

<div class="responsive-video-container">
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezi.com/zosfs2" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>


### Tools
- Sketchfab - 3D model repo
- Blender - reducing poly count, change pivot points
- Bezi - early design and interaction setup 
- Unity 2022.3.16f1 - low-poly prototype development, added smoke and audio


### Project build versions & hardware
- Unity 2022.3.16f1
- Meta XR SDK All-in-one 60.0.0
- Bezi Unity Bridge 0.1.3
- Meta Quest (v2 onwards)


## Challenge

The goal of this assignment was to create a Meta Augment for our room for entertainment, wellbeing or productivity. For those that don't know what Meta Augments are, their goal is to provide virtual funcionalities across our physical spaces. Think of them as 3D interactive widgets that get stuck in your room.

<div class="responsive-video-container" style="padding-bottom: 620px;">
  <div class="fluid-width-video-wrapper">
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Meta Spark - Quest 3 Augments showcase.<br><br>Haven&#39;t seen this around and I&#39;m not sure if it has been published widely/publicly yet. <a href="https://t.co/kCfALl8Upm">pic.twitter.com/kCfALl8Upm</a></p>&mdash; Luna (@Lunayian) <a href="https://twitter.com/Lunayian/status/1743888916233556417?ref_src=twsrc%5Etfw">January 7, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
  </div>
</div>


The first part of the assignment was to gather a set of 3D assets that turn your room into a place that you have been thinking of from sketchfab in which the total number of vertices should be lower than 100K.

The second part of the assignment was after the initial selection, make a possible Meta Augment for your room.

**Since we had less time to make a prototype (2 weeks), I chose to make a simple widget for meditation. Prepare a incense candle and have music and light help me in my meditation. As I wanted smoke and sound in my prototype, I used Unity and Meta's building blocks to achieve that in the end. So let's dive right in.**


### Asset selection in Sketchfab - Stage 1

On Sketchfab, selected around 10 assets related to meditation:
- Spaces
  - [Meditation space](https://sketchfab.com/3d-models/meditation-e9252c4f99ce4dcba4710fb42da403ab)
  - [Meditation diorama](https://sketchfab.com/3d-models/meditation-diorama-a8e5d404631348aab2a64046f9aaf263)
- Statue: **[Buddha](https://sketchfab.com/3d-models/buddha-d8e644bba0794c53bc16f4728e7d78f4)**
- Incense Holders and candles
  - **[Incense](https://sketchfab.com/3d-models/incense-44fecf4227ae49b0a322abc8841eb310)**
  - [Incense sticks](https://sketchfab.com/3d-models/incense-sticks-nag-champa-atchouli-b8b21230410d4c3ebca9e205e06f8925)
  - **[Copper incense holder](https://sketchfab.com/3d-models/copper-incense-150fc8e73a464a56a2d1d5f8fde5662a)**
  - [Dragon incense burner](https://sketchfab.com/3d-models/dragon-incense-burner-fb16dc0f855546a5bcb61237acb51efd)

- Meditation bowls
  - *[Singing Nepali Bowl - Animation](https://sketchfab.com/3d-models/singing-nepali-bowl-animation-68d135abd71f400fa47f55a85ac3db19)*
  - [Tibetan Bowl](https://sketchfab.com/3d-models/tibetan-bowl-18f4d2cca6944b058fc41566e239c350)
- Orbs
  - *[Magical Orb](https://sketchfab.com/3d-models/magical-orb-5e2e0ac919cb4d30ac022133086c088c)*
  - **[Orb of Chi](https://sketchfab.com/3d-models/orb-of-chi-5b9b6b38c601459e95b24184d68e3255)**
- Music/Audio
  - [Relaxing song for meditation](https://freesound.org/people/Antenalosmusic/sounds/711662/)

I narrowed them down to those in bold for these factors:
- Prettyness (example: the selected incense candle look prettier than the bag of incense sticks)
- Poly count (everything above 100k excluded, like the dragon incense burner); and its topology (not sculpted models - models with relatively straight lines and more polygons for added realism on bending points)
- Usage of normal maps for added realism instead of additional poly count (example: the buddha and copper incense holder)
- Usability (if I had time, I would have added a meditation bowl for additional sound interaction - but it was not the main thing for the experience so I cut it out from the final prototype)
- Issues with shaders: the shader used for both orbs were not supported by the gltfast package used by Bezi Bridge. I didn't have much time and just wanted a nice looking orb - so the orb of Chi with some minor import changes looked pretty for prototyping purposes. 
  - If you want to dwell on the topic, here is a description of the technical issue - apparently I could have [imported the additional shaders by API](https://github.com/KhronosGroup/UnityGLTF?tab=readme-ov-file#unitygltf-and-gltfast), due to this [KHR_material_variants issue](https://github.com/KhronosGroup/UnityGLTF?tab=readme-ov-file#unitygltf-and-gltfast). 

Regarding the poly count, topology and rendering maps - I used sketchfab layer tool to check each model wireframe and maps. You can see the gallery below to see how it sketchfab model inspector helped selecting the assets.

{% include gallery id="gallery-sketchfab" caption="Screenshots of analyzing assets on sketchfab and the list of possible candidates at the end" %}


### Asset alterations in Blender - Stage 2

Used blender to perform asset alterations in order to be used in my Bezi design.
- reduce poly count by using the decimate modifier. 
- changed the pivot point for some models. Examples: 
  - the Buddha, and incense holder pivot point to the floor so it would be easier to set on any table;
  - the incense candle in the non-burning tip where people should usually hold it
- removed or split 3D models in parts so that I could use each separately (and changed their pivot points as well):
  - Singing Nepali bowl had both the bowl and the stick. Created assets for each and imported them to bezel.

{% include gallery id="gallery-blender" layout="half" caption="Screenshots of the blender projects with changes made" %}


### Early design prototype in Bezi - Stage 3


![My project in Bezi]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/07/bezi-augment-design.png)

The first design for the meta augment that I made was in Bezi. I choose Bezi to help me concretely think in how the interactions in igniting the incense stick might work, and what sort of effects I could use.

You can see the video and interact with it. As you might be able to see, I tried to use the import the orb - but the shaders used are not available in Bezi (and also in Unity).

{% include video id="919694261?h=910ddc48e7" provider="vimeo" %}

***Attention: to trigger the incense animation you have to click on it, but since it is quite a small object - it is a bit hard.***

<div class="responsive-video-container">
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://bezi.com/zosfs2" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
  </div>
</div>


### Gather everything in Unity - final stage 4


![The good "old" unity development with Bezi Bridge]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/07/good-old-unity-module07.png)

Here I essentially [reused my previous project in Unity from module 06](../xr-design-fellowship-module-06-assign/), and performed:

- similar setup work like in module 06 (building blocks for: interactable, grabbables, synthetic hands setup; and from the Meta unity sample projects: snap objects)
- some slight modifications in the Custom Bezi Animation script to be able to include external Unity Events (like dimming/brighting the lights, play/stop music, start/stop the smoke effect)
- some minor bug fixes in my snap processing stages (like making sure initial stage was disabled to help guiding the user to actually start the meditation)
- changed from the [Magical orb](https://sketchfab.com/3d-models/magical-orb-5e2e0ac919cb4d30ac022133086c088c) into the [Orb of Chi](https://sketchfab.com/3d-models/orb-of-chi-5b9b6b38c601459e95b24184d68e3255), because the package dependency that bezi integration uses (gltFast) did not support these types of materials - and so its animation never looked cool.
  - therefore I made my own simple animation of having the orb going up and down to inspire deep breathing
  - and performed some material adjustments on the orb of chi. 
- smoke effect using a particle system 
- simple light brighting/dimming script 

The implementation time was much faster because I had learned from my previous mistakes and I tried to keep it as a simple as possible due to the time frame.

I think it turned out much better than the bezi original idea. Don't you think?

{% include video id="919653214" provider="vimeo" %}

You can access the [project's repo here](https://github.com/tiagomms/xrdf-module06-bezishapes-unityIntegration) or you can actually [test the project build by downloading this folder](https://drive.google.com/drive/folders/1NxvkJMxLp5KyMjOVTRlYb42K0vj-_kBh?usp=share_link) into your Meta Quest.


## Issues

### Hardware:
- Only works with Meta Quest. 
- Next stage would be use to Unity XR Framework to expand usage or to Vision Pro with eye tracking


### Technical issues 

Same as in [module 06](../xr-design-fellowship-module-06-assign/). I didn't even tried to change anything there.


### Design:
- Did not test actual Grabbing (did not have time but it makes total sense, once it is on someone's table). 
- that being said, it will be very important to enable/disable grab or distance grab based on user's distance (possibly putting a very large sphere collider around the incense object) - not implemented yet
- Improve the snapping part. Sometimes it does not transition between states. Did not have time to debug this very closely.


### Feedback

(coming soon)


### Next Steps

- Add basic UI for meditation management (change lights according to type of meditation/chakra) - like a chakra orb record player
- if it makes sense, some meditation bowl & drums, but that actually might bloat the augment


## Conclusion

Before this module, I was unaware of how many details Sketchfab provided to us in inspector mode. And to learn these simple edits in Blender, it just makes total difference when prototyping for XR, and to help everything be as performant as possible.

Thank you [Aniol Masó](https://www.linkedin.com/in/aniolsaurinamaso/), [Billy Kwok](https://www.linkedin.com/in/billykwokhk/) and the whole XR Bootcamp team for this module! 

