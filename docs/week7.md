# WELCOME BACK

## Review: Setting a Default Level
To set a default level to open in the editor or game from Project Settings
- Navigate to Project > Maps & Modes > Default Maps.
- Set `Editor Startup Map` and `Game Default Map` to your desired default level's map.

## Opening & Reloading Levels
The Open Level nodes are used to immediately switch to a  new level, either by name or by reference. Reference is very convenient if you are setting the level by hand (and is also not prone to typos!). 

Delay nodes can be used to wait before continuing to perform actions in Blueprints, which is often nice when you're switching levels as it makes the transition less jarring.

Key nodes:
- [Open Level (by Name)](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Game/OpenLevel_byName?application_version=5.4)
- [Open Level (by Object Reference)](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Game/OpenLevel_byObjectReference?application_version=5.4/)
- Delay

### Ignoring Player Movement Input
It's common to temporarily need to disable player input at different times. For example, when a delay is being used just prior to switching levels.

The Get Player Controller will reference the Player Controller set in Project Settings. Once referenced, the Set Ignore Move Input node can be used to enable and disable movement controls.

Key Nodes:
- [Get Player Controller](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Game/GetPlayerController?application_version=5.5)
- [Set Ignore Move Input](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Input/SetIgnoreMoveInput?application_version=5.5)

### Camera Fade In & Out
Bonus! Here's a simple way to create a fade in/out transition effect from a solid color using Get Player Camera Manager. This node will return a reference to the player's camera manager in the level, which will allow you to use the Start Camera Fade node to create a timed transition of the alpha channel of a color.

To fade in:
- Connect the two nodes to a Blueprint's Event BeginPlay node.
- Set From Alpha to 1.0 and To Alpha to 0.0.
- Set Duration in seconds and then check the Hold when Finished box.

To fade out:
- Connect the two nodes to a Blueprint's Event node which manages the level ending actions. (This might be a Custom Event).
- Set From Alpha to 0.0 and To Alpha to 1.0.
- Set Duration in seconds and then check the Hold when Finished box.
- Additionally, if you are using this to fade out a level, use a delay node with the same duration before the Open Level node.

Key Nodes:
- [Get Player Camera Manager](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Game/GetPlayerCameraManager?application_version=5.5)
- [Start Camera Fade](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/CameraFades/StartCameraFade?application_version=5.5)

## Working with Components (Blueprints)
Components in Blueprints are referred to using variables. To manipulate a component, drag its variable into the Event Graph. From there, you can search for the name of the property you want to manipulate.

Key Nodes:
- Set Visibility 

## Working with Sound (Part 1/2)

### Simplest way to play a sound: Play Sound 2D
To play a sound with no attenuation, you can use the Play Sound 2D node. It is designed for non-gameplay sounds such as UI, but can be used for in-game sounds as well (uncheck the Is UISound box).

### Importing Sound Files
To import audio, drag your `.wav file` into the `Content Drawer`. Important: convert your audio to wav files _before_ importing.

# Homework

## Fall Break Next Week
Take some time off!

## Continue Open Exploration Project 1 (Due 10/21)
The project description can be found [here](project1.md)

### This week:
Find time after the break to _nearly_ complete your project. Things will need to be completely finished by 5pm on 10/21.

### Important: What to turn in, where, and when
In the `lastname_firstname_project1` folder you created for homework last week, add the following:

- 3 high quality screenshots from UE5 which shows different views of your completed project. _Don't forget to toggle Game View to remove the XYZ orientation widget._
- Completed Unreal Engine Project. _Make sure to upload the project folder and all of its contents!_
