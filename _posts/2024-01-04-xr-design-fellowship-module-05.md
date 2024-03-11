---
title: "XR DF Module 05 - Mixed Reality and Co-location Experiences"
date: 2024-01-04T20:00:30+01:00
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
header:
  image: /assets/images/xr-bootcamp/xr-design-fellowship/module/05/live-session.jpeg

---

Here is a glimpse of what I have learned during Module 05 of the XR Design Fellowship program!
Sorry, but this is a bit of extra work for me (that helps a lot), but becomes difficult to manage.

As usual, I am mostly paraphrasing experts and centralizing the learnings we get from them and the XR Design Fellowship team. For me this is mostly a learning summary of what I have learned this month.

## Glimpse of our module: Mixed Reality and Co-location Experiences

With the launch of Quest 3 and the upcoming Vision Pro, the promising potential of Mixed Reality has grown even more - as the blending between virtual and real worlds becomes more and more a reality!

Our project was to create a MR fitness experience with real-time feedback and interactions, with a safety first mindset and adaptable to sizes and shapes of different physical spaces, or have some sort of social interaction. 

**I focused on exercises to make people fit while in Bed (hence FitInBed). I wanted to do something for people that can't barely walk (due to muscular degeneration or inactivity after surgeries) and thus have a lot of limitations when it comes to exercising. The fact they stay in a bed without moving much leads to higher chances of respiratory infections, and thus these sort of games/fitness exercises would certainly help on that regard**.

You can find more information and see the project development in this post:
- [Module 05 Assignment - Designing MR Fitness Game: FitInBed Game - Get out of my porch](../xr-design-fellowship-module-05-assign/)

On Nov 8th we had an amazing live session with [Mo Sayyar](https://www.linkedin.com/in/mohammadsayyar/) (Design Leader and Former Design Director @ FitXR). [Paul Hoover](https://www.linkedin.com/in/pahoover/) joined at the end of the Q&A session for a few more insights.


## Live Session

### Expert introduction
*This introductory part is a copy of their Linkedin and EventBrite descriptions - I am not reinventing an introduction here*

[Mo](https://www.linkedin.com/in/mohammadsayyar/) was previously the Director of Design at FitXR, a Senior Product Designer at Gravity Sketch, Design Lead at Tvroi, and Design Manager at Gamesys. He oversees various design domains, including product design, game design, concept and 3D design, technical art, and marketing design.

[Paul](https://www.linkedin.com/in/pahoover/) has been designing emerging technologies for the past twenty years in Seattle. At Microsoft, he worked on Tablet PCs, the massive multitouch Surface, and Windows touch applications. Then, he worked at Artefact for emerging tech clients like Samsung, Intuitive Surgical, Magic Leap, and Facebook Reality Labs. At the time, he created an immersive design tool called StoryboardVR to help accelerate the Artefact design team's creating experiences for Magic Leap. After designing AR communication experiences and games at Meta for three years, he returned to creating design tools. He is heading up design at ShapesXR, trying to accelerate the XR industry.

### Takes

This session was truly insightful, as it was the first talk we had on MR and the differences from VR and AR. Honestly, I will be copying/paraphrasing most things, because Mo's level of insight on product design and MR is really profound - I don't see myself adding anything here.

Anyway I tried to write *exact quotes from Mo* this way. 

#### MR Basic Principles

- ***MR is the symphony between the real and the imagined.*** (loved that quote). In MR **the integration between digital and physical objects is really important, because how the experience feels and behaves is the main thing for users**.
- When designing for VR/MR context is key - that is why you should design with VR Tools immediately (ShapesXR, Gravity Sketch). In MR you immediately start thinking of interactions around the objects you want it to occur (bed, chair, ...) and that speeds up your product to market. Context and actual perception is lost with flat screen tools (even Blender rendering with several viewpoints). (It was already mentioned on previous talks, but this note reinforces the importance of developing and using XR tools for design).  

- Basic Principles of MR: 
  - **Spatial Awareness: navigation and interaction between physical and digital objects should be seamless as possible**.
  - **Intuitive Interactions: To do that designers should focus on the root physical interactions (examples: use a knife, spoon, opening a door...) to reduce cognitive load. Remember besides gestures, voice commands may help**
  - Visual hierarchy: our job in 3D space is to direct users in what to see, and indicate the relationships between elements (with colors, size, placements). **It is really easy to lose focus and flow of the app in MR - this was not the case with flat screens because people usually can only focus on one frame at a time due to hardware limitations (it was something we were blessed and never considered before)**
  - Performance Optimization: we should be aware of our target device limitations. 
    - If we plan cross-platform usage, we should reduce the features to the minimum common denominator in terms of hardware and technology (unless we know ahead that we need specific technological features, but that may reduce our market share).
    - In addition, help the development team to minimize latency in terms of rendering, visuals, tricks and perhaps different algorithms
  - Acessibility: inclusivity is something important to have present for different users (example: main hand configuration - right or left)
- ***In MR users are the center of a dynamic environment. Thus, we have to design for multiple spaces, backgrounds we don't know and it is extremely important to understand where they will use it (airport, car, house, gym, ...,) and how (acessibililty features)***
  - ***In MR the cognitive load is usually higher because we are not in full control. So our experiences should enhance and not overload - and that is done through user research***

#### Tools & Technologies for designers
- ***We should never let tools or lack of tools hold you back as a designer.*** Right now, Mo usually uses:
  - Figma with XR plugins (such as Layerbeam to preview layouts in VR/MR)
  - For the sake of prototyping: Blender + free 3d assets (from sketchfab, turbosquid or Text-to-3D generative AI like [Luma genie ai](https://lumalabs.ai/genie)). You don't need mega modelling skills, just be able to adapt free assets to your needs and render them with viewpoints.
  - Unity with VR low-code frameworks: VR Builder / VRIF - for usability testing and actual make interactive prototypes
  - ShapesXR:  *it is the best tool for prototyping and VR/MR design out there because it doesn't require technical knowledge. It is very easy to put and show ideas to stakeholders. It also enables you to understand basic user interactions and make simple usability tests for observation*. (I agree with Mo here)
  - other tools not as relevant: Gravity Sketch, Google Blocks, Adobe substance modeller, ...

#### Design best practices (the best part of the talk personally)

- **User comfort**: avoid eye strain, motion sickness, hard to look - hard to follow, body fatigue, visual fatigue. ***Our goal should be that whatever you put, solves a problem for the users (just because we no longer have limitations when it comes to what we can put in front of the users, that shouldn't be green pass to put everything we can out there)***
- **spatial mapping and awareness**: most mapping is done by the hardware/software provider, but we should always design in a manner that replicates real world behaviours. 
- **The frame from which the user sees**. Example: something to look at shouldn't be at the same distance from something you interact with 
- **Interaction models**: design should reflect how users interact with both physical and digital elements (it includes: gesture, controls, voice commands, and traditional input methods)
- **Intuitive UX elements: familiarity in MR is more important than in VR** (in VR you place elements in your space and are in full control), in MR there is always a point of reference so learning curve should be rather small - it is very encouraged to use common design patterns.
- **Use of spatial sound to provide cues about the environment, interaction and actions**. Its goal is to direct the focus of the user experience
- **Environmental considerations: MR experiences should adapt to different physical environments and in multiple scenarios (light, space size).** 
  - An example provided was a fitness competition: how can you make an experience in which someone is in a 2x2m and another in a 6x6m have the same score? 
  - In FitXR they 3D capture different environments and test them in ShapesXR and Unity to reach a conclusion.
- **Accessibility**: it is important to keep it accessible for all users, but we need always to keep in mind the level of the experience and the user base we are targeting
performance: already discussed
- **Global vs Local design**: **We should consider the OS provider global design guidelines even though we may not be full on board with their decisions** (example: iOS apps - Apple forces you to follow guidelines, to ease onboarding. Because of this you end up feeling everything as part of a global system). ***Remember that users are already going through a learning curve (of how to interact with the device and the OS). If it takes a very cognitive load for the user to learn the device, plus your app, people will not use it.***
- **Iterative design & testing**: very important to have tools for very fast prototyping that can be used by users
- **Balance of aspirational & practical: *in MR and new technologies hype gets in the way (people want to do something different, but forget what was done previously and want to reinvent everything from scratch);*** It is important to keep the sense of business in mind (otherwise no funding, user base, product and work for us).
- **Challenges in MR Design: *Challenges in MR are as diverse as the environments it encompass, which can affect how real or digital an object feels within a space***.
  - Technical limitations when it comes to tracking accuracy or lighting conditions; 
  - Different and various environments (size, lights, background sound, ...)
    - example: An app used outdoor in sunny locations should have a different design an app used in safe indoor small spaces (like a bed).
  - Safety (never design actual risky chores with your quest 3 - like cutting vegetables)
  - Localisation: use images/animations/sound cues for more and better direct ways to communicate - avoid using text
  - **Practicality: *Doing MR for MR sake is not a good idea, always try to solve a problem and have the users in mind***.
    - Great practical app example: [PianoVision](https://www.meta.com/experiences/5271074762922599/) (kind of a guitar hero to actually learn piano). Once you do the tutorials, you are forget about MR, and focus on your goal that is to learn the piano.

#### Future Predictions
- It is important for designers to bring new use cases that could happen in the future (for remote working, training, education...)
- Help evolve XR Software to facilitate creation (with low code/no code, like ShapesXR) 

#### Mo's personal recommendations
- On developing projects: 
  - squeeze time on pre-production, design; more time on production and user testing (this way it allows you to adapt more and be more iterative). 
  - Try to start testing since the first layer of interaction is ready (something playable, not polished)
  - If you need more higher fidelity, you need more moderated sessions to see and observe. To excel designs, Mo usually benefits more from these sessions by defining goals, user flows, tasks for users and observe users without helping them on succeeding tasks.
  - avoid biases: get a set of user testers - do a very short call with each to understand and categorize them into groups. Then, it is also important to categorize people during the observation if a bias is sensed. But instead of avoiding, dismissing or ignoring the person, try to regulate the insights of the session differently.

- For Skills designers:
  - In general: **Becoming really good at problem solving and being able to articulate your idea to not just a design team, but shareholders and developers. For this, the ability to bring something visual for better alignment is really important.**
  - Hard skills (softwares): 
    - be really good at UX design, Figma, know XR plugins
    - ShapesXR is still not know in the industry, but learn it
    - know a bit of how to use 3D modelling software (not necessarily professional modelling) - do a few screenshots, renders, change materials, adapt
    - Unity (85% experiences are designed there) - use VR Builder, or VR Interaction Framework (those add-ons are not easy to use, but you could learn how to prototype ideas)
  - Soft skills: being able to dettached from their designs - being the hardest critic of their own work
  - For MR testing: there are no external tools for testing accessibility and adaptability of the experience. It is really important to help the developing team to develop tools internally to solve problems.
  - basic mistakes: doing MR for MR sake instead of thinking of user problems, and reinventing the wheel is never good enough 
    - ***if something is good on 2D there is no need to change, unless you have valid info that flat UI is somehow hurting the user experience.***
  - storytelling: very important for new interactions, new user flows (clean and understandable for the users and stakeholders)
  - it is important to have a user testing group for personal projects that are willing to share their time with you (30 minutes a week/month). It is also important to keep them engaged.

- On new technologies:
  - the most important part is to find ways that the user interface and experience really allow more use cases and more accurate use cases. **Sensors and hardware can be there, but the way the technology is used and shaped for the consumer - that is the most important part**
  - for fitness: VR was very limiting due to safety, you cannot move that much. With color passthrough and depth sensor - activities that require your body to move further (run, or use real weights like dumbbells, Pushups towards the walls) may become possible. And with that you can bring more exercises, harder difficulties, more time spent in actual experiences, and walk around and experience your surroundings.
  - on the upcoming vision Pro: *essentially thinking there is a business plan/ ecosystem with apple devices only is a bad idea (we don't know when they will ship, how many, or when ...), and the skillset doesn't exist at the moment. We are relying on them to actual build our products. Quest pro is probably the best way to prototype for the vision pro due to the eye tracking functionality (but it is very different in terms of resolution and quality)*

## Assignment after live lecture

As mentioned earlier, you can find more information and see the project development in this post:
- [Module 05 Assignment - Designing MR Fitness Game: FitInBed Game - Get out of my porch](../xr-design-fellowship-module-05-assign/)

## Conclusion

As mentioned previously, it was a very insightful session and I don't think I have much to add to what Mo has said. It was really impressive to experience the level of depth that Mo had on product design and how to apply it to MR.

The main thing that was different from other sessions and what got stuck in me was the importance of cross-platform testing and the importance of designing with a mindset for stakeholders, developers and our users. We are not reinventing the wheel, and sometimes (even if we didn't want to, or disagree) we have to adapt our designs to a global way of doing things, to smooth the onboarding experience for everyone.

It is quite a revolucionary field that is coming. And I was and still am very happy to be apart of this session. 

Thank you [Mo](https://www.linkedin.com/in/mohammadsayyar/), [Paul](https://www.linkedin.com/in/pahoover/) and the [XR Bootcamp team](https://xrbootcamp.com/) for providing this opportunity to learn from you. It has been a privilege!