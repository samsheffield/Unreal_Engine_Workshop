# Overriding Game Modes, Game Instances, and Audio Integration

## Reminder: External Hard Drive
I have two external hard drives that you can use to submit classwork each week if you are struggling with online storage caps. Please keep things organized.


## Today:
- Review
- New things
- Review homework (after lunch)
- Work session

## Quick Review
_First, a quick review!_
- Keeping score
- Review the basic setup and interaction patterns of UI (Binding text to variables and clicking buttons)
- Setting up functions

## World Settings
Each Level can have unique settings applied to it from the World Settings panel. This includes activating particular Game Modes for levels.

### To open the World Settings panel:
Select the `Settings` icon at the top right of the toolbar and then choosing `World Settings`.

Note: This will open World Settings as a tab next to Details.

### Overriding Game Modes
This is helpful if you have one Game Mode that is handling the majority of your game's code, but have the need for different code on specific levels.

#### 1. Create a new Game Mode Blueprint 
Right click in the `Content Drawer` > `Blueprint Class` > then choose...
- _Basic Game Mode_ (good for UI): `Game Mode Base`
- _Starter Content Game Modes_: Search `All Classes` for `BP_ThirdPersonGameMode` (for example)

This is called _deriving from a parent class_ which means that our new class _inherits_ all of the functionality and properties of its parent.

#### 2. Set GameMode Override
To override the default Game Mode, just select your level's Game Mode in the `Override Game Mode` dropdown of the `World Settings` panel.

## The Game Instance
A Game Instance is a high-level manager object for an instance ot the running game. It is created when the game is started and destroyed when the game is closed and persists between levels. 

It is a handy place for you to put variables which you need to use across multiple levels.

Important note: __There is only one Game Instance per game.__

### Setting up a Game Instance

#### 1. Create a new Game Instance
Right click in the `Content Drawer` > `Blueprint Class` > then search `All Classes` for `GameInstance`.

#### 2. Set the GameInstance
- Open `Project Settings`, then navigate to `Maps and Modes` > `Game Instanc`e (at the bottom of the list).
- Set the `Game Instance Class` to your GameInstance Blueprint.

### Setting and getting variables in GameInstance

#### To set a variable in the Game Instance
- Create a variable in your Game Instance (I'm referring to the variable as YourVariable and the Game Instance as `BP_YourGameInstance` below).
- Nodes:  `Get Game Instance`-> `Cast to BP_YourGameInstance` -> `Set YourVariable` (from the `As BP_YourGameInstance` output pin).
- Connect the Set node to the output of a node which is providing the updated data.

#### To get a variable in the Game Instance
- Create a variable in your Game Instance.
- `Get Game Instance` -> `Cast to BP_YourGameInstance` -> `Get YourVariable` (from the `As BP_YourGameInstance` output pin).
- Connect this output to a node which is using this data.

## Integrating Audio

### Importing audio
To import audio, drag your `.wav file` into the `Content Drawer`. Important: convert your audio to wav files _before_ importing.

### Sound Cues
The audio output of the combination of nodes created in the Sound Cue Editor is saved as a Sound Cue. Sound cues are used to set audio, pitch, and volume of sounds played in a level.

#### Creating a new Sound Cue
- Right click on your audio file in the `Content Drawer` and select `Create Cue`.
- Name it with the prefix `S_`.

### Sound Cue Editor
The Sound Cue Editor is used to mix and design the sound played by a Sound Cue.

To open the editor, double click on a Sound Cue in the `Content Drawer`.

#### Audio Node Graph
The Audio Node Graph is located in the `Viewport` panel. It displays the audio signal path from left to right, with interconnected nodes representing audio control modules and audio files. 

The `Output` node, which has an image of a speaker on it, represents the final output of audio as heard in-game and is always positioned furthest to the right in the signal path. `Sound Wave files` are always positioned furthest to the left in the signal path. Wires are used to connect the nodes.

For a full list of audio nodes see [the documentation](https://docs.unrealengine.com/4.27/en-US/WorkingWithAudio/SoundCues/NodeReference/). 

#### Previewing Output
To preview playback, use the play buttons located in the toolbar at the top of Sound Cue Editor window.

The `Play Cue` button plays the entire Sound Cue, and the `Play Node` button plays the sound from the selected node. 

### Creating Background Audio

#### 1. Create Sound Cue
Convert your wav file into a Sound Cue (Right click and `Create Cue`). 

#### 2. Set the audio to loop
Open the Sound Cue in the Sound Cue Editor by double clicking it. Select the Wave File in the `Audio Graph`. In the properties panel to the left, check the `Looping` box under `Sound Wave`. Save the Sound Cue.

#### 3. Add to the level
Drag the Sound Cue into the level to add the background audio to the level. Adjust volume in the Sound Cue Editor by selecting the `Output` node and adjusting the `Volume Multiplier` property.

### Spatialized Audio
It is easy to create spatialized, 3D audio in you levels using Sound Cues.

#### Attenuation
The key to 3D sound is _attenuation_. Attenuation effects how the sound fades or changes relative to the position of the player. Overriding attenuation allows you to enable spatialized audio.

Attenuation settings include:
- Volume: How the audio fades
- Spatialization: How the sound is positioned in 3D space
- Occlusion: How sound is affected by the 3D objects in space
- Reverb: How sound echoes in a space

### Adding spatialized Sound Cues to a level

#### 1. Create Sound Cue
Convert your wav file into a Sound Cue (Right click and `Create Cue`). 

#### 2. Override attenuation
Open the Sound Cue in the Sound Cue Editor by double clicking it. Select the `Output` node in the `Audio Graph`. Check the `Override Attenuation` property in the `Attenuation` heading. This will reveal all of the attenuation settings for the Sound Cue. `Enable Spatialization` should be checked by default.

There are two important properties which affect the spatialization of a Sound Cue. They are both under Attenuation (Volume):
- Inner Radius: This determines where the attenuation effect begins. Within this radius, audio is played at full volume.
- Falloff Distance: This is the distance of the fading effect that begins outside of the Inner Radius.

Some other helpful options:
- You can adjust the `Override Attenuation` settings in the Details panel in Scene View.

#### 2A. Set the audio to loop (optional)
Select the Wave File in the `Audio Graph`. In the properties panel to the left, check the `Looping` box under `Sound Wave`. Save the Sound Cue.

#### 3. Add to the level
Drag the Sound Cue into the level to add the background audio to the level. Adjust volume in the Sound Cue Editor by selecting the `Output` node and adjusting the `Volume Multiplier` property.

### Using a Sound Cue as a sound effect
For simple sound effects the Play 2D Sound Blueprint node is limited but effective. To use a Sound Cue requires a little more setup but allows for spatialized audio.

Key nodes:
- [Play Sound At Location](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Audio/PlaySoundatLocation/)

# Homework

### Soundscape Exploration
For this assignment, you will be creating a small explorable level which uses Sound Cues to reward and encourage curiosity. 

This should begin at a start screen, switch to a game level, and then finally switch to an end screen which can return to the start screen with a keypress.

_You are welcome to build upon any other classwork you've created for this class thus far._

In the start level:
- Add a Sound Cue which plays as background audio
- Some text that onboards a player
- A button or text prompt which instructs players to start.

In the game level:
- Create an environment which has at least 3 instances of spatialized audio. One should be randomized when approached.
- A goal which switches to the end scene.


In the end level:
- Display some text that wraps up a player's experience (optional: this text changes based on a Game Instance variable)
- A button or text prompt which instructs players to restart.

You will need:
- A Game Mode for the game level and one for the start level
- Wav files (You may want some of these to loop)
- Optional: A Game Instance to hold a variable which selects text to display in the end scene 


#### Important: What to turn in, where, and when
You can either upload the work to your class Drive folder (preferred) or transfer it to my external drive next week.

#### Zip your files before uploading
Please zip your Unreal project folder and name it `yourname_week11_uew.zip` before uploading it. Otherwise, the files may become corrupted in the process.