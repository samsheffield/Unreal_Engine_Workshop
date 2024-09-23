
## This Week: Blueprints Intro
- What's a blueprint?
- How to create a blueprint
- What's a collider? Overlapping vs Blocking
- Using Cast To nodes to check an Actor's type
- Print a message for testing
- Destroy an Actor
- Keep track of things with variables
- Creating Sustom Events

## What is a Blueprint?
Blueprint has more than one meaning in Unreal Engine.
1.  It's the name of the visual scripting language used in the Unreal Engine. 
2.  It's a type of complex game object created using the Blueprint language.

There are two main types of Blueprints: 
- Level Blueprint: Each Level has its own Level Blueprint (and only one).
- Blueprint Class.  These are used to create interactive objects which can be reused in any Level.

## Blueprint Resources:
- Unreal Engine Blueprint documentation can be found [here](https://docs.unrealengine.com/5.4/en-US/blueprints-visual-scripting-in-unreal-engine/).
- Blueprints Visual Scripting for Unreal Engine 5 - Third Edition ([link](https://www.packtpub.com/product/blueprints-visual-scripting-for-unreal-engine-5-third-edition/9781801811583)).

**This week's notes on materials can be found [here](week5_bpnotes.md)**

## Work Session & 1-on-1 Meetings
In the second half of class, I'll meet with each of you to check your homework from the past two weeks. Please have your materials ready.


# Homework

## Week 5 Homework: Interaction Study

_Note: You are welcome to either start from scratch or add to your Week 3 & 4 homework._

Create a level in UE5 which encourages interaction between Actors through collision/proximity. Give your player a goal and use simple interaction a means to accomplish the goal in an _interesting_ way.

Criteria:
- Create a Blueprint for an interactable Actor (this interaction will be based on collision).
- Create a copy of BP_ThirdPersonCharacter and add at least one variable which keeps track of player interaction.
- Design an interation which either Destroys of Spawns an Actor in the level.Or both! 
- You are expected to recreate the Blueprints we demoed in class today. Please do not use the Blueprints we already created together.
- All Blueprint nodes need to be commented (either individually or in groups).

### Important: What to turn in, where, and when
Add a new folder to your root folder in the class drive called `lastname_firstname_interaction_study`. In this folder, add the following by the start of class next week (09/30):

- The Unreal project. Make sure to include the _entire_ project folder and _all_ of its files! 
- 3 high quality screenshots from UE5 which shows different views of your lit and textured map. _Don't forget to toggle Game View to remove the XYZ orientation widget._

