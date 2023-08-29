---
title: "XR DF Module 02 - Concept Ideation and XR Storyboarding"
date: 2023-08-21T20:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
  - ShapesXR
toc: true

---

Here is a glimpse of what I have learned during Module 02 of the XR Design Fellowship program!

## Glimpse of our module 

Although methodologically similar, XR ideation differs from traditional UI/UX ideation in a key way. Spatial design is inherently hard to visualize and communicate among designers, making it more difficult to co-ideate and co-create than flat experiences. 

Fortunately, tools are being developed to tackle these challenges - mainly [ShapesXR](https://www.shapesxr.com/product) - a XR Prototyping tool created specifically to tackle the problems designers have. 

The goal of this module was to learn how to ideate and create a XR storyboard, in order to understand what works and does not in 3D environments and avoid the pain of developing full immersive experiences only to figure they don't work (thus saving a lot of time).

Here are this module's learning goals:
- Set up your ideation and storyboarding environment using the recommended spatial design tools.
- Understand and practice XR ideation workflow through mood boarding and spatial co-ideation.
- (Pre-assignment) Create a “Gaze-and-pinch” Smart Home experience by storyboarding how users interact with your design.
- Learn about how ideation and storyboarding are done in the industry (with Paul Hoover).
- (Post-Assignment) Incorporate the design techniques mentioned in the lecture into your prototype refinement for the post-assignment.

This month's live session was with the great [Paul Hoover - Head of Design for ShapesXR](https://www.linkedin.com/in/pahoover). We learned a lot from him.

**Live Session from Paul Hoover**
![Live Session - Gaze & Pinch Interactions in Smart Homes]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/02/live-session.png)

## Live Session

Here a few takes of the session:
- Creating "spatially" requires proper tools, since our world is not flat and 2D screens cannot capture the sense of scale, distance, spatial properties, new input types (hands, gaze, voice) and new digital ways of handling experiences in 3D space (Virtual Reality, Augmented Reality, Passthrough, ...).
  - The result of not having these tools are long development cycles with unpredictable results
  - ShapesXR allows Ideating and prototyping right in the 3D space, and export to our favorite game engines and 3D modelling softwares; and it is already being used by Meta.

- Spatial storyboarding is really important to simulate experiences as fast as possible, and test & throw ideas as soon as you can. 
  - Since the technology is so new and has so many factors, Co-ideation is really important because if you can't simulate yet, "Wizard of Oz(it)" - fake the interaction and show how it would work to others.
  - With ShapesXR mocking mechanics is no longer needed - you can just import your things and work it out.

- Our bodies and our brains will become more and more entangled in these experiences. If not thoroughly prototyped/tested, an experience that could feel like magic can become a nightmare. 
- This is specially important for gaze & pinch interactions.
  - **Our eyes do not work as a "mouse", they are incredibly unreliable for tracking, but can be great for context**. This is because our eyes most common movement is saccades - dart around (see image below)
  - It has been thoroughly tested: **if your eyes were a cursor, you'd be chasing your eyes and not the cursor.**

- So how to design experiences with gaze?
  - **We don't have control of our eyes, so our goal is make the user not think about their eyes.** Otherwise, severe eye strain and exhaustion can occur.
  - **Gaze only for context. As designers and developers, we need to work towards just noticeable differences**.
    - Just noticeable differences are experiences where the majority of users understand what they need to do when gazing, but not over do-it so it is not uncomfortable. Fading / easing interactions becomes super important
      - Note: For now, it appears there aren't people overly sensible to these differences (maybe people with lazy eye)
  - Gaze for context + Pinch / pinch drag is by far the best interaction.
  - Never have very small targets - follow the Apple guidelines size of at least 1.6 degrees from you for interaction and add some padding to minimize errors 
  - When you are about to get/perform direct touch on (virtual) objects, our eyes automatically look at where the next action should be.

  ![Live Session - Gaze & Pinch Interactions in Smart Homes]({{ site.url }}{{ site.baseurl }}/assets/images/xr-bootcamp/xr-design-fellowship/module/02/saccades.png)

- Thoughts on the vision pro?
  - Due to privacy concerns, there might be complications between Unity apps and vision pro, because we may not have access to dwell/hover interactions
  - the design for multi-modal system experiences (voice, hands, gaze, in-air gestures) can be amazing and make actual better tools and human-computer interactions. 
  - it is possible that Apple may design at least 1 controller (like the magic leap 2) due to amount of limited interactions that your hands can do.

- Great Gaze & Pinch interactions:
  - Microsoft Mesh for Hololens 2 (according to Paul, the best developed product with gaze & pinch until now)
  - Gaze for Context on SideQuest (video below) - good interactive introduction

{% include video id="StXDwpouhkM" provider="youtube" %}

### How tricky is eye tracking

**This linkedin post is really good - The art of eye tracking**

<div class="responsive-video-container">
  <div class="fluid-width-video-wrapper" style="padding-top: 56.25%;">
    <iframe src="https://www.linkedin.com/embed/feed/update/urn:li:share:7084548728543440896" height="1569" width="504" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen title="John LePore - The art of eye-tracking"></iframe>
  </div>
</div>

## Assignments

Both assignments have their own post. Check them out:
- [Pre-Assignment: Mood & Storyboarding in Figma & ShapesXR](../xr-design-fellowship-module-02-pre-assign/)
- [Post-Assignment: Refine Prototype to Higher Fidelity in ShapesXR](../xr-design-fellowship-module-02-post-assign/)


## Personal Thoughts

Before the bootcamp, I haven't had much experience follow the process of ideation, brainstorming, storyboarding and prototyping without code. It is really beneficial for my personal practice and reduces a lot of stress.

I can say with the ShapesXR team ([Jeremy Casper](https://www.linkedin.com/in/jercasper/), [Paul Hoover](https://www.linkedin.com/in/pahoover/), [Gabriele Romagnoli](https://www.linkedin.com/in/gabriele-romagnolixr/), I realized it is relaxing and actually fun to prototype things.
ShapesXR makes you feel like you are playing with play-doh or painting, or playing piano. 
It can be a very smoothing experience and I appreciated that a lot.

Thank you to the XR Design Fellowship team, and ShapesXR for this incredible module!




