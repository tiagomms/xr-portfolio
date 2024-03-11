---
title: "XR DF Module 07 - 3D Asset Pipeline for XR Prototyping"
date: 2024-03-10T20:00:30+01:00
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
  image: /assets/images/xr-bootcamp/xr-design-fellowship/module/07/live-session.png

---

Here is a glimpse of what I have learned during Module 07 of the XR Design Fellowship program!
In the [previous module 06](../xr-design-fellowship-module-06-assign/) we did not have an expert session (it was a tutorial based module as intro to Unity), but this month we had the privilege of having [Aniol Saurina Masó](https://www.linkedin.com/in/aniolsaurinamaso/), hence this article!

As usual, I am mostly paraphrasing experts and centralizing the learnings we get from them and the XR Design Fellowship team. For me this is mostly a learning summary of what I have learned this month.

## Glimpse of our module: 3D Asset Pipeline for XR Prototyping

We have been advancing in our XR prototyping work (it has been 8 months now!), but we never had a module on how to streamline our XR design process when it came 3D asset handling. The goal of this module is mostly to understand and learn what should a XR Designer know about 3D modelling tweaking, prototyping and importing.

Since the module 06 took longer than expected, this module was supposed to be smaller. **Our goal was to create a simple Meta Augment for our room for entertainment, wellbeing or productivity. I focused on a simple meditation augment to help your meditation in MR passthrough.** You can find more information and see the project development in this post:
- [Module 07 Assignment - Turn my room into a meditation center](../xr-design-fellowship-module-07-assign/)

On February 22nd we had an amazing live session with [Aniol Masó](https://www.linkedin.com/in/aniolsaurinamaso/) (Former Senior XR Designer and Prototyper @ Masterpiece Studio). 

## Live Session

### Expert introduction
*This introductory part is a copy of a Linkedin and EventBrite descriptions*

[Aniol](https://www.linkedin.com/in/aniolsaurinamaso/) has been a Designer and Creative Technologist for the past ten years. His most recent work has focused on designing and prototyping spatial experiences for a wide range of platforms, including a VR app for creators available in the Quest Store, room-scale art installations showcasing internationally, a set of VR simulations used in educational research, and AR applications built in collaboration with cultural institutions, among others. Some of the areas he’s focused on in the past include product design, 3D design, UI/UX, physical and digital prototyping, front-end development, and product strategy.

### Takes

This session was really a great intro to the 3D asset pipeline in XR Design. I will be copying/paraphrasing Aniol, because he really prepared a great presentation.

Anyway I tried to write *exact quotes from Aniol* this way. 

#### Intro

- 3D Model Components: very basic intro into what are meshes, quads vs triangles, unwrapping (the unfolding of a 3D mesh into a 2D plane), bones, skinning and animations.
- Use cases for 3D assets and their differences: 
  - 3D Printing: must take into account gravity and physics constraints
  - Pre-rendering (mostly for film production, major pre-calculated simulations) - no direct interaction 
  - Real time rendering: *user has agency and control of situation (vs pre-render situation) and it requires a lot of optimization. It is all is happening in real time in a machine, thus developers need to optimize things. In XR that becomes even more important (recommended 90Hz frame rate) to avoid any motion sickness*.

#### 3D Asset pipeline for XR prototyping:

- Due to motion sickness mentioned above, this pipeline becomes super important.
- The 3D source and knowing their limitations is really important: 
  - AI models very quick to make but are not optimized and not user friendly to change; 
  - 3D asset scanning requires asset cleaning; 
  - creating models is most times consuming except very simple prototypes
  - best option is really online libraries: because they are optimized for real game engines, but tend to exist issues with copyright
- When importing models it is really important to know the asset polygon topology, LODs and thinking about of removing polygons not visible: 
    - **The Goal: low poly object with great visual fidelity. Aim for as little polygons as possible**
    - Still check topology (wireframe) of the model. Parts that bend requires more polygons, Straight things (like an arm), should have quite a straight line. 
    - ***3D modelling becomes always a compromise between ragged edges (from afar - see face) and number of vertices***
    - Sculpting models is not used in XR - because the process focus on detail (only the final shape is important) and not on poly count / performance
    - a great option to reduce poly count: use decimate modifier in blender to optimize number of vertices
    - In XR apps, it is really important to apply Level Of Detail (LODs) to reduce number of polygons and texture map resolution based on distance. In Unity the process is quite simple to do, but for that you need to create/tweak models in blender and import them to unity after.
    - Removing polygons not visible (cut them) by using bissect in blender is key to reduce poly count.
    - Always think of model's point of reference (or pivot, origin) in where you want to pivot the object based on position,rotation, gravity... 
      - you can do it in unity, but it is good practice to do in 3d modelling software so it will be like this everywhere 

- Next step is to think on the models materials that cover the mesh. The most recommended material type is physically based rendering (pbr) with additional maps for added realism: 
  - metalness - grayscale map in which white is more metallic; black less - like skin/clothes
  - roughness - is almost the opposite of metalness; the more rough (white), less shiny it is;
  - normal map - add detail without geometry (just based on this image) does not compromise computer power, it reacts to light and provides shadows and details in the mesh, without polygon change.
    - Normal maps are usually created by 3D artists in which they transfer the detail from a high poly version of the model into a texture, through a projection from high to low poly. Then they use adobe substance painter to paint over it.
  - ambient occlusion - adds sub-shadows on ambient light 
  - opacity - it is a transparency map (trick use planes with transparency)

- Another important topic when tweaking models is the UV Mapping. When we look to paint a 3D mesh we use the method of unwrapping the 3D mesh into a 2D plane that we call UV Map.
  - if well made, we could go to photoshop and change something immediately instead of loading a 3D modelling software (like changing a text or basic colors)
  - if badly made, like automated UV Mappings, the translation between UV map and 3D model is not 1-to-1. Model edges are disconnected in the UV map, making it difficult to make simple changes 

- Lastly, animations: first you need to check the rigging and skinning. 
  - In sketchfab, most times the impacted skin area by bones are colored in the same color as the bone. Their tonality represents the bone importance of morphing the object. 
  - humanoid animations use [mixamo](https://www.mixamo.com/#/) - it is very quick to use. It automatically creates the skin and provides the animation map for your imported character

#### Basic 3D modelling techniques - Blender mini tutorial

In the end, Aniol performed a quick sketchfab and blender tutorial of basic 3d modelling techniques. 

  - In Sketchfab: learn how to use model inspector, check topology, and other maps
  - In Blender: 
    - import object in file format and make sure everything is alright
    - how to change pivot point
    - axis snap with (mouse wheel press + alt)
    - find out object polycount in blender
    - see object wireframe
    - decimate to reduce poly count further
      - Note: Decimate in collapse mode is good, but too much "decimation" will affect the UV map. If you are a 3D artist then you may manually readjust the UV map, but it is a balancing act.
    - select whole mesh with x-ray button
    - bissect to cut non-visible parts and reduce poly count further
    - export file and apply modifiers. Choose export format according to end interface:
      - web: gltf - allows to change texture separate (modify directly) 
      - pc: fbx - camera, lights, bones, animation (a lot of info) 
      - obj - does not support animations 
      - apple: usdz - there are known issues regarding texture conversion from other format into this one. [Feel free to checkout Sketchfab page about this](https://help.sketchfab.com/hc/en-us/articles/360046421631-glTF-GLB-and-USDZ).
      - textures recommmended size for XR: 1024 x 1024
      - Unfortunately, exporting the desired file format is not a warranty for everything that was done stays exactly as expected due to legacy file formats, conversion limitations or something else - always test the end result! 
  - In Unity - procedure to get models:
    - export fbx and include textures in blender 
    - move model to unity 
    - solve misconfiguration issues: 
      - to get textures it is required to extract them first through the extract textures button
      - then set normal maps as normal maps and if needed, change the material render pipeline

#### Last notes

- Aniol said that the basic techniques he showed, and basic 3d modelling skills for creating rough prototypes (not covered in the module - but things like from a cube, create a very rough car approximation) should be enough for XR Designers to excel.
- The good thing about 3D modelling: once you know the basics (like extruding) you should be able to do all these basic things in any software.
- But 3D is not always the way to go. Examples: 
    - particles for smoke skybox for elements far away (like shadow of colussus) 
    - baked lighting or fake shadows/lights with 2D planes with painted gradients. This is how Vision Pro looks, but actually they use a 2D plane mesh to simulate ambient lighting main spots, and then the models infer from those light points and generate shadows
    - other techniques: 
      - use plane, textures and alpha masking (transparency) to give 3d perspective to usually very complex models (hair, tree tops); 
      - remove parts not visible from mesh (example: tree roots or floor below game area (because you will never see it))
- Regardless of what you do in your computer, always test, test, test your models in XR 
  - Things like stairs or door frames in a computer might look fine, but in XR they need to have the right dimensions (otherwise our our 6th sense might feel something is wrong and the sense of immersion might break).

## Conclusion

As mentioned previously, it was a very insightful session and great introduction to 3D Modelling in this field. Aniol was super generous in breaking the presentation in small learning bits, and then provide a tutorial that was recorded internally for us to see in blender.

I used these techniques in Sketchfab, Blender and Unity for my assignment. Feel free to check it out: 
- [Module 07 Assignment - Turn my room into a meditation center](../xr-design-fellowship-module-07-assign/)

Once again, thank you [Aniol](https://www.linkedin.com/in/aniolsaurinamaso/) and the [XR Bootcamp team](https://xrbootcamp.com/) for providing this opportunity to learn from you. It has been a privilege!