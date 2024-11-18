# Creating Movement

## Demo video
I will have a video of today's demos uploaded by tomorrow (just needs editing!)

## Assets for today's Demo
[Here is a link](https://drive.google.com/file/d/1UvXVqyHmepPoWlY-raefQ6H5vevsMpnJ/view?usp=sharing) to some assets for this week's demos (courtesy of Mixamo.com).


## Actor Mobility
For any actor which moves, the Mobility setting underneath Transform needs to be set to Movable. If not you will get a warning (or several!) to remind you to set this.

## Rotating Movement Component
There are [some basic components](https://dev.epicgames.com/documentation/en-us/unreal-engine/movement-components-in-unreal-engine) which can be used to add movement to a Blueprint Instance.

## Blueprint Timelines
_Timeline nodes are special nodes within Blueprints that provide time-based animation to be quickly designed and played back based on events, floats,vectors, or colors that can be triggered at keyframes along the timeline._

Unreal Documentation is [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/timelines-in-unreal-engine). Unreal also provides a couple of nice examples, such as [this one](https://dev.epicgames.com/documentation/en-us/unreal-engine/fading-lights-in-unreal-engine) for fading and changing coloration of a light.

### Useful Nodes
- Add Timeline
- Set Play Rate
- Lerp (Vector)
- Set Relative Location

## Spline Movement
The Spline component combined with a Timeline can be used to create a path for movement.

### Useful Nodes
- Get Spline Length
- Get Location at Distance Along Spline (Set Coordinate Space to World)
- Get Rotation at Distance Along Spline (Set Coordinate Space to World)
- Lerp (float)
- Set Actor Transform
- In Construction Script: Set Actor Location and Get Location at Spline Point (Set Coordinate Space to World)

## Adding Animation
FBX models and animations can easily be imported to Unreal Engine by dragging them to the Content Drawer. Note: Animations need to be connected to a Skeleton on import, so it's best to import the model for the Skeletal Mesh first so you can than select it when importing animations.

## Skeletal Meshes
Meshes that can be animated are called Skeletal Meshes. They are associated with an underlying Skeleton (also known as a Rig) which is used to move and deform the model.

## Playing Animation Assets
When you add a Skeletal Mesh to the level, or to a Blueprint, you can set the way it will play an Animation Sequence. The easiest is to change set the Animation Mode to Use Animation Asset in the Details panel. You can also select the Animation Sequence, and control automatic playback and looping from here as well.

### Useful Nodes
- Play Animation (Be sure to set the Animation Asset)

## Animation Blueprints
For more complex animations, you will want to use an Animation Blueprint to manage the playback of multiple Animation Sequences based on rules.

### State Machines
Animation Sequences can be put into State Machines, which allow you to transition from onesequence to another using different rules.

# Homework

## Player Retargeting Demo
I will post a video demonstrating how to retarget the default mannequin's animation to a new skeletal mesh. That means, you will be able to replace your player's mesh AND animation (finally!)

- Retarget the player's skeletal mesh.
- Replace the Run and Walk animations.
- Fix the Animation Blueprint
- Create one actor the follows a Blueprint spline that moves in a loop.

__For this demo, I want you to work with a character and animations from Mixamo.__ If you can get it to work successfully, then you are welcome to try it with your own rigged character. In Blender, you can use the Rigify plugin to accomplish this or you can upload your mesh to Mixamo.


### Important: What to turn in, where, and when
Add a new folder to your root folder in the class drive called `lastname_firstname_animation_study`. In this folder, add the following by the start of class next week (11/25):

- The Unreal project. Make sure to include the _entire_ project folder and _all_ of its files! 
- 3 high quality screenshots from UE5 which shows different views of player and moving actor. _Don't forget to toggle Game View (press G key) to remove the XYZ orientation widget._
