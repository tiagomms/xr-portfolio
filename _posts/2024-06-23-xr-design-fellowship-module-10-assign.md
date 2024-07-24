---
title: "XR DF Module 10 - Assignment: Design Augmented Product Experiences using Meta Spark Studio"
date: 2024-06-23T17:00:30+01:00
categories:
  - blog
tags:
  - XR
  - Spatial Computing
  - XR Design
  - XR Design Fellowship
  - XR Bootcamp
  - Augmented Reality
  - Meta Spark Studio
toc: true
header:
  video:
    id: 966068797
    provider: vimeo 
gallery-ar-library:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-menu.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-menu.png
    alt: "Meta Spark New Template menu"
    title: "Meta Spark New Template menu"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-arlibrary-01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-arlibrary-01.png
    alt: "Meta Spark AR Library Sketchfab Cereal box Model"
    title: "Meta Spark AR Library Sketchfab Cereal box Model"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-arlibrary-02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-arlibrary-02.png
    alt: "Meta Spark AR Library Sketchfab Toy Model"
    title: "Meta Spark AR Library Sketchfab Toy Model"
gallery-stage-02:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-patcheditor-02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-patcheditor-02.png
    alt: "Meta Spark AR Debug on Simulator Patch (set false when testing in production)"
    title: "Meta Spark AR Debug on Simulator Patch (set false when testing in production)"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-patcheditor-01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-patcheditor-01.png
    alt: "Meta Spark AR Open/Close Lid animation by patches. It includes the scaling box particles after some delay (changed in the box particles inspector)"
    title: "Meta Spark AR Open/Close Lid animation by patches. It includes the scaling box particles after some delay (propriety which changes are enabled in the box particles inspector)"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-boxparticles-cerealbox.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/metaspark-boxparticles-cerealbox.png
    alt: "Box particles implementation and Meta Spark Studio Interface. Check out the scale is different from the rest - it means its value can be altered in a patch"
    title: "Box particles implementation and Meta Spark Studio Interface. Check out the scale is different from the rest - it means its value can be altered in a patch"
gallery-stage-04:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/patch-toy-transform-changes-01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/patch-toy-transform-changes-01.png
    alt: "The whole patch section of changing the toy position, rotation and scale"
    title: "The whole patch section of changing the toy position, rotation and scale"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/patch-toy-transform-changes-02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/patch-toy-transform-changes-02.png
    alt: "Zoomed in part of the first image. Variable isGiftReady and how it pulses/enables different behaviours. This changes the toy rotation, scale and position (not the box - I had a label mistake there)"
    title: "Zoomed in part of the first image. Variable isGiftReady and how it pulses/enables different behaviours. This changes the toy rotation, scale and position (not the box - I had a label mistake there)"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/patch-toy-transform-changes-03.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/patch-toy-transform-changes-03.png
    alt: "Creating a script producer patch - it took a while to find that out. It was key to send values from scripts and trigger changes in the patch"
    title: "Creating a script producer patch - it took a while to find that out. It was key to send values from scripts and trigger changes in the patch"
gallery-feedback:
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/feedback-module-10-01.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/feedback-module-10-01.png
    alt: "Sergei feedback part 1"
    title: "Sergei feedback part 1"
  - url: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/feedback-module-10-02.png
    image_path: /assets/images/xr-bootcamp/xr-design-fellowship/module/10/feedback-module-10-02.png
    alt: "Sergei's feedback part 2"
    title: "Sergei's feedback part 2"

---

## Module 10 Assignment - Meta Spark: Digital gifts with gravity coming out of a box


You may access the [project's repo here](https://github.com/tiagomms/xr-metaspark-flyingObject/tree/main) or you can actually [test the project build by downloading this folder](https://drive.google.com/drive/folders/1tAvD_4XGMKg2Xp6v-0rL2dBttz4vv27G?usp=sharing) into your Meta Spark Studio and test it on device. 


### Tools
- Meta Spark Studio v178 
  - Cannon js light physics add-on
  - Sketchfab models add-on. Models retrieved from Meta Spark AR Library: 
    - Malik Do Kyanon
    - strawberry_smiggles_cereal_box


## Challenge

The goal of this assignment was to design a product experience using Spark Studio in this module. Examples of product experiences include product discovery, product exploration, product try-on, etc. 
I was asked to ideate and design a prototype, that needed to fulfill the following requirements:

- Demonstrate how an XR experience may help potential customers make their buying decisions
- Make use of plane tracking or target tracking
- Interactive (device motions, device rotation, touch input, etc)
- Egocentric (looking outward away from the user)
- Overlay virtual content on top of a fixed physical object or a physical spot

This was my first time using Meta Spark Studio - so I wanted to do something simple, and then it got complicated.

### Why Meta Spark Studio?

For now, Meta Spark focus is for Augmented Reality Filters and simple games, using the front/back camera of smartphones. 
However, it all indicates that Meta Augments may only be developed using Meta Spark.

If you don't know what Meta Augments are, their goal is to provide virtual funcionalities across our physical spaces through Meta Quest headsets. Think of them as 3D interactive widgets that get stuck in your room.

As people use headsets more and more, this feature may become quite ubiquitous - so learning Meta Spark becomes super important.

<div class="responsive-video-container" style="padding-bottom: 620px;">
  <div class="fluid-width-video-wrapper">
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Meta Spark - Quest 3 Augments showcase.<br><br>Haven&#39;t seen this around and I&#39;m not sure if it has been published widely/publicly yet. <a href="https://t.co/kCfALl8Upm">pic.twitter.com/kCfALl8Upm</a></p>&mdash; Luna (@Lunayian) <a href="https://twitter.com/Lunayian/status/1743888916233556417?ref_src=twsrc%5Etfw">January 7, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
  </div>
</div>

## From ideation to the actual prototype

My original idea was to have a real cereal box, that once the back camera detected a image target on it, it would simulate opening the box, and have toys fly. Once these toys landed on the table, they should be interactable. 
The inspiration came from real-life hoping to get the toy you want from the things you ate as a kid. 
But another use cases include: collecting objects (trade, interactive, NFTs), getting discounts for shows, and lastly basic games. 

**What I ended up doing (in the video): once the target image is detected, a virtual cereal box appears and an open box animation starts. It throws towards the sky an interactable toy that lands by the bottom of cereal box, that you can interact with (by changing position, rotation, scale).**

The reasons why the original idea, and subsequent ideas fell through:
- actual object recognition/ knowing the lid dimensions would be quite impossible to do in a systematic way. To actually fake it, I would need to spend a very long time trying to hardcode lid dimensions and floor distances that could never be replicated. I also believe that based on the distance that the camera detected the pattern, all these values could change. 
- For this reason, I thought in starting the experience with the virtual cereal box and use Spark's multiplane tracking to choose to place it in a spot, like [the Spark multiplane tracking tutorial](https://www.youtube.com/watch?v=JJUCzRDC9oU&t=414s). Once that was done, the image tracking would show up, and from that point, the box would open and the toy would fly. But:
  - Spark only allows either world tracking or image tracking, not both at the same time (not even toggling is available). That took a longer time to figure out than expected.
  - I realized the Patch editor would not help me out with providing the physics for the toy, and for that I would need to use code and CannonJS specifically. It was unexpected and required much more development time, as there aren't good tutorials on cannonJS and meta spark with cannon js. 
  - I had already the image tracker in the experience. It would be easier to ignore the world tracking bit, instead of remaking most of early experience.
  - **For some reason, for a week or 2, the Meta Spark templates menu did not provide any good template. They magically appeared once part of the development was already made.**
  - This was my first Meta Spark experience, I was learning as I went.
- Reduce experience to one single toy. Adding others would present further complications and complexity in the patch editor and app management. As an example: how to know for which object a screen tap, pinch, rotate was intended - would be a new design problem on its own. Therefore, focusing on a single object made sense.


I know this was not the intended case study that I wished to do, but for the time I had - it was the best I could do. Now I will describe a bit of the actual concept development.

### Stage 1: choose template; AR library - get sketchfab models, patch editor first changes

Step 1: Since I thought I didn't need to code, I chose a template that just used patches. 
At the time, Meta only provided me a template with a image tracking - that once the target was found a geometric object would start rotating. 
Later on, once Meta provided more templates, I copied by hand this other template that tracked objects using patches. 

Step 2: Meta Spark AR Library with its integration to sketchfab works quite well. I added the two free models: a cereal box that included a lid and a toy (Malik).
I had to make a few changes in each imported model (remove clutter, change pivot point, etc.). All in Meta Spark (they were very simple to make). 

{% include gallery id="gallery-ar-library" caption="Screenshots of the Meta Spark initial experience" %}


### Stage 2: Cereal Box - Patch Editor and Particle Effect 

- Create open and close lid animations. They took quite a while to figure out because there is no way to send the delay value between opening each part of the lid (they must be hardcorded).
- Use a Debug Pulse to show and close the lid in the simulator.
- Created a particle effect when opening the box. Can't make particle effects invisible, so the trick is to control the particle scale (hack promoted by Meta)
- Once it was working fine, placed the toy inside the cereal box

{% include gallery id="gallery-stage-02" caption="Screenshots of the Patch Editor and Particle effect implementation" %}

### Stage 3: Scripting

As mentioned, coding became a necessity when there was no way to add physics to the toy by patch. 
On the AR Library, we could add a lightweight script package for physics called Cannon Js.
I haven't coded in Javascript for quite some time, and there isn't that much documentation on Cannon JS, so it was tricky.

The weirdest thing in the physics development is that physics bodies are created independently from the actual mesh objects, and it is not possible to set the physics body/collider as a component of the actual mesh object. The only existing solution was to create an invisible flying physics box and an invisible ground plane, so that in every frame calculate where this invisible flying box was - and set the toy position equal to it.

By the time all code was working, the script did the following things:
- found the toy, and cereal box
- created physics world with gravity
- created a physics body for the toy, and a ground plane below the cereal box 
- subscribed to two events: on opening the cereal box (openBox), and on losing the tracking (resetBox)
- on opening the cereal box, an upward force is applied on the toy to make it fly
- when flying, created an event that in every frame sets the toy position to be equal to its physics body representation
- on colliding on floor, the flying physics event is destroyes, and the toy becomes ready to be manipulated by the user on his screen. 

The major technical issues I had while developing : 
- performing operations between Meta Spark and Cannon JS. Despite having the same name, Meta Spark Vectors (Reactive.Vec) was a different type from CANNON.Vec (so a lot of undefined errors started to occur)
- Getting the surrounding box size of toy proved to be quite hard (the bounding box value always returned the same amount despite changing scale). I ended up hardcoding some box value that looked similar.
- Some weird bug occurred with CANNON.Planes - it only worked well if the cannon body was created first, and later add the shape (instead of doing it all at once). 
- transformValue and worldTransformValues on Meta Spark may not match the transform CANNON values, which meant a possible need for matrix manipulation if this ever went to production.
- (stage 4) getting values from script and add them to a patch. This was important for changing the toy transform only after flying and landing on the ground plane; and even more importantly to reset the changes once the target tracking was lost. 
- (stage 4) Super annoying thing: once an object position (or something else) was changed via script, any patch changes for it were ignored (the field became disabled and could only be changed by script). For someone, that had done a lot via patch, this was a big nuisance (example: I had written a function to Reset the toy position, but if used, it was no longer possible to increase the toy rotation/scale via patch).


### Stage 4: Refinement; Patch editing the toy

I had copied the template from Meta Spark to scale and rotate an object using patches. The goal was to apply it to the toy. It took a while to figure out to get script values to enable/disable these capabilities, because of the issues mentioned above.

To solve this, it was added to the toy: 
- a null "parent" object (Malik): its position, scale and rotation could change and reset via patch. To do so, used if/then/else blocks to either enable changes via screen tap, pinch, rotate if target was being tracked or reset otherwise
- a null "grandparent" object (Malik-rifle-root): its position would change with the CANNON body; and reset the original location via script once the tracking was lost

Then I had to: 
- Create a producer patch of the scripts - to get the boolean value isGiftReady (for scaling / rotating)
- have a pulse that: 
  - in case is on (true): it enables the screen contact to change the toy parent position, rotation, scale;
  - in case is off (false): it resets the parent position, rotation, scale
- an if/else block makes sure there are no bugs when changing the position, rotation, scale. The condition is based on the value of the boolean isGiftReady 

{% include gallery id="gallery-stage-04" caption="Screenshots of the final Patch Editor" %}

***Image disclaimer: (wrong label in the second image) where the colored boxes say Box Position, Rotation, Scale, they were actually Toy Position, Rotation, Scale.***

At last, the template had an interactive tracking image instruction that I kept while the image target is not found. Since it was hardcoded (by the script provided by Meta), I just kept the block and variable names.


## Feedback

This month's expert [Sergei Galkin](https://www.linkedin.com/in/sergeyglkn/) liked the project.

I asked him month's expert [Sergei Galkin](https://www.linkedin.com/in/sergeyglkn/) some questions on the two main issues I had regarding the patches/script interoperability and Spark's limitations on multi tracking systems on the same prototype. Below, his replies on the topics:

{% include gallery id="gallery-feedback" layout="half" caption="Feedback on project by this month's expert Sergei Galkin" %}

### Next Steps

- It appears there is a bug when I redo the animation many times. The toy gets projected higher and higher (perhaps I need to clean up the forces in the toy).
- Being able to include more toys and differentiate each screen tap, rotation, and pinch (probably by using tap as a selecion method; and then the other gestures; or have a UI to select and sliders)
- change from target to world tracking, to place the virtual cereal box on the ground or table, and then perform the animation part
- add sound effects
- make UI/UX to collect the toy and display its rewards (if it makes sense) 
- keep using Meta Spark


## Conclusion

I saw a lot of value for the use cases Meta Spark promotes (face filtering, simple ar content pop up). There are a lot of templates provided my Meta and it appears a cool way to learn more about shaders with real time changes. The sketchfab integration works quite well.

But once you get out of the use cases provided - you really need to know the inner workings of it all (that I couldn't find any reference in the documentation). 

I kind of got bummed out for things like:
- not being able to use both an image target and plane tracking on the same demo (even toggling one for the other is not possible)
- changing values by code locks any external changes via patch editor
- there isn't a nice way to import different project templates into a main project (if projects start to get more complex, this may become an issue) 
- limited use cases (it may be considered normal as it was focused for face filters, and simple ar content).
- did not explore this: but it appeared there was no way of debugging scripts in real time (except by Diagnostics.log)
- lack of coding examples for physics related stuff 
- integrate with unity/unreal/game engines - especially if things start to get trickier and more features are included

Then again, the good thing of Meta Spark is that it is being constantly updated. And once a version for Meta Quest 3 comes out, it should bring a lot of nice features :)

Thank you [Sergei Galkin](https://www.linkedin.com/in/sergeyglkn/), [Billy Kwok](https://www.linkedin.com/in/billykwokhk/) and the whole XR Bootcamp team for this module! 

