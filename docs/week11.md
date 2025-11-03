# W E L C O M E ! !

Today, we'll meet as a group to discuss:  
- Importing Skeletal Meshes and Animations  
- Creating and Using Animation Blueprints  
- Controlling Animation States  
- Creating Control Rigs using the Modular Rig Tool  
- Animating Skeletal Meshes and Actors in the Level Sequencer  
- Level Sequencer Basics

---

## Video Demos

Weekly demo videos can be found on our class Canvas Welcome page. I will have new videos posted no later than Wednesday evening most weeks.

Need a specific demo? Let me know!  

---

## Reminder: Unreal Engine 5.6 Documentation

In addition to what we cover in class each week, the best place to look for additional information is  
[the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation).  

---

## Skeletal Animation Systems in UE5

This week, we’ll introduce the Skeletal Animation System in Unreal Engine 5.6.  
You’ll learn the difference between Animation Sequences, Animation Blueprints, Control Rigs, and Level Sequencer workflows and when to use each one.

---

### Importing Skeletal Meshes and Animations

- Import FBX models with embedded skeletons and animations (or using separate FBX files)
- Review FBX Import Options:
  - Skeleton: None (creates a new skeleton)
  - Check "Import Animations" if your animation clips are included in your FBX
- Inspect imported Animation Sequence assets  
---

### Creating and Using Animation Blueprints
An Animation Blueprint is used to structure the logic of animated states. These can be controlled with other Blueprints.

We'll create a simple state machine with two transitions and trigger it from an interaction in the level
---

### Playing Animations via Blueprint
- Open your Character Blueprint  
- Add logic to trigger animations
- Use Play Animation and Get Anim Instance nodes

---

### Creating Control Rigs with Modular Rig

- Right-click on your Skeletal Mesh → Create → Control Rig  
- Choose Modular Rig  
- Add simple keyframes by adjusting bone transforms (for example, rotate arm or hand)  
- Animate using keyframes directly in UE with the Level Sequencer
- Bake to Animation Sequence 

Discussion:  
- Animation Blueprint = runtime logic  
- Control Rig = in-engine animation creation  
- Level Sequencer = cinematic control  

---

### Using Level Sequencer and Creating Cutscenes

- Create a new Level Sequence  
- Add a Skeletal Mesh Actor  
- Add Animation Track → select your imported animation or Control Rig  
- Add Transform Track → move actor through the scene  
- Add Camera Cuts Track → use CineCameraActor for shots  
- Animate a simple sequence: character enters → waves → exits  

### Triggering Sequences from Blueprints

- Add a Trigger Box in the level  
- In its Blueprint:
  - On Begin Overlap → Play Level Sequence  
- Add Visibility Tracks to hide or show actors as needed  

---

## Week 11 Homework: Animation System Study (Due 11/10)

### Assignment Details

Create a short animated scene that combines skeletal animation systems in Unreal Engine 5.6.

Your project should demonstrate:
- Imported skeletal mesh and animation  
- Basic Animation Blueprint with Idle → Some Other State transition  
- Simple Control Rig animation using Modular Rig  
- Level Sequencer cutscene using a CineCameraActor  
- Blueprint logic that triggers the sequence  

### Estimated Completion Time: ~5 hours

Focus on learning how these systems connect. Keep your models simple. Clarity and understanding of animation flow are more important than detailed assets.

If any part seems to be taking particularly long, reach out to me via email or visit our TA in the Game Lab on Wednesday afternoon for guidance.

---

### Deliverables

Create a folder in your class drive named:  
YourName_GMD265_11

Include:
- Unreal Project Folder: complete project with Level Sequence, Animation Blueprint, and Control Rig setup  
- Screenshots: at least 3 images showing different moments in your animation  
