# W E L C O M E ! !
So excited to welcome you all back from the holiday. Today, we'll meet as a group to discuss...
- Introduction to Blueprints
- Managing Levels/Maps
- Physics and Collision

We'll also...
- Door Problem + Video
- Review your homework from week 2

## Video Demos
Weekly demo videos can be found on our class Canvas Welcome page. I will have new videos posted no later than Wednesday evening most weeks.

_Need a specific demo?_ Let me know!


## Reminder: Unreal Engine 5.6 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation). Check it out!

---

## Level Design and the Door Problem (Revisited)

<iframe width="560" height="315" 
src="https://www.youtube.com/embed/AYEWsLdLmcc" 
title="YouTube video player" 
frameborder="0" 
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen>
</iframe>


## Blueprints
- What's a Blueprint?
- How to create a Blueprint
- What's a collider? Overlapping vs Blocking
- Using Cast To nodes to check an Actor's type
- Print a message for testing
- Destroy an Actor
- Keep track of things with variables
- Creating Custom Events
- Changing levels/reloading current level

### What are Blueprints?

In Unreal Engine, _Blueprint_ can mean two different things:  

1. Blueprint as a Language  
   - Unreal Engine’s built-in _visual scripting language_, which lets you create gameplay logic without writing C++ code.  

2. Blueprint as an Asset 
   - A type of _reusable game object_ that can include actors, components, and Blueprint graphs to define behavior.  

### Two Main Types of Blueprints

#### Level Blueprint  
- Each Level has _one (and only one)_ Level Blueprint.  
- Useful for managing events specific to that Level.  
- Less flexible, since it can’t be easily reused across multiple Levels.  

#### Blueprint Class  
- Can be attached to Actors to create interactive, reusable objects.  
- Works in any Level, making it modular and scalable.  

### Our Approach in Class

While Level Blueprints have their uses, they’re limited in flexibility and not ideal for long-term projects.  

We’ll focus on Blueprint Classes (Actor Blueprints) because:  
- They encourage modular design.  
- They’re easier to reuse and maintain.  
- They align with professional workflows in game development.  

---

## Blueprint Resources:
- **This week's notes on materials can be found [here](week4_bpnotes.md)**
- Unreal Engine Blueprint documentation can be found [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/blueprints-visual-scripting-in-unreal-engine?application_version=5.6).
- Blueprints Visual Scripting for Unreal Engine 5 - Third Edition ([link](https://www.packtpub.com/product/blueprints-visual-scripting-for-unreal-engine-5-third-edition/9781801811583)).

---

## Bonus Materials: Physics

### Important: Actor Mobility
- Actors have three Mobility settings: Static, Stationary, and Movable.  
- For any Actor that moves, set `Mobility` to `Movable` under the `Transform` section in the Details panel.  
- Note: If not set correctly, Unreal will display warnings until you fix it.

### Applying Physics
1. In the Details panel, locate the `Physics` section.  
2. Check `Use Physics` (if not already enabled).  

#### Adjusting Mass
- Mass is calculated automatically based on the Actor’s size.  
- Use the `Mass Scale` property to multiply the base mass by a custom value.  

---

# Homework

## Week 4 Homework: Interaction Study (Due 09/22)

### Assignment Details
This week you will create a small new project in Unreal Engine focused on basic interaction.  

Your task is to design a simple level where the player can interact with objects through collision or proximity and trigger outcomes such as resetting the current level or moving to a new level. Use the level's design to complicate the player's ability to interact with the objects.

Consider the relationship to the player has to the objects and why they might want to interact with them.

### Assignment Goal
The purpose of this exercise is to introduce Blueprint scripting for interaction. You will learn how to:  
- Create interactable Actors using collision or overlap  
- Trigger outcomes that reset the current level  
- Trigger outcomes that move the player to a new level  
- Organize and comment your Blueprint logic clearly  

### Important Steps

**1. Create a New Level**
- Start with a new empty level in UE5 using the `FirstPerson (No Variant)` template.
- Add a simple floor and _at least_ two objects the player can interact with  

**2. Create Interactable Actors**
- Make a Blueprint Class for an interactable object  
- Add a Collider Component (you choose the appropriate shape!) and set it to trigger overlap events  
- Test the interaction using Print String before adding more complex outcomes  

**3. Design Interactions and Outcomes**
- One interaction should reset the current level.  
- Another interaction should load a different level.  

**4. Comment and Organize**
- Try rebuilding the Blueprints we demonstrated in class, but do not copy and paste from shared files.  
- Add comments to your nodes so the logic is easy to understand and also to remind you to ask for help where something is unclear.  

### Deliverables
Create a new folder in your Picasso class drive folder named:  
`Lastname_Firstname_GMD265_04`

In this folder, include:  
1. **Unreal Project Folder**: The complete project folder (not just the .uproject file). _Please don't forget to hide the UI gizmos!_  
2. **Screenshots**: At least 3 images showing your level and the interactions taking place.  
3. **Short Reflection**: 1 –2 paragraphs describing:  
   - The interactions you designed  
   - How you set up the reset and level change outcomes  
   - Any challenges you faced and how you solved them  

### Tips and Reminders
- Keep it simple! This assignment should take no more than 5 hours. 
- Make sure interactable Actors are set to Movable in the Details panel if needed for physics.
- Test interactions frequently in Play Mode  
- Use Print String to debug before adding more complex behavior _but don't forget to remove them once done!_  
