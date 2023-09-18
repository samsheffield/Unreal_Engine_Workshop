# Continue getting familiar with the Unreal Editor
Welcome back Today, we'll meet as a group to...
- Continue getting familiar with some of the basic operations of UE5.

## Review Warm-up Explorations
Let's spend some time taking a look at everyone's weekend explorations.

## Blank Template (Starting with a clean slate)
The empty template is great to work with when you need a clean slate to work from, but seeing a black screen in the Viewport can be a little confusing at first. At minimum, you probably want:
- A Directional light actor
- A SkyAtmosphere actor (from Visual Effects)
- An ExponentialHeightFog actor (from Visual Effects)
- Optional: A Skylight actor
- Optional: A box brush to create a ground surface (from Geometry)

You can add these actors individually, but the lighting can be added more quickly using the Environment Light Mixer panel.

### Environment Light Mixer
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/environment-light-mixer-in-unreal-engine/)

The Environment Light Mixer is an editor window where you can create and edit a Level's environment lighting components for sky, clouds, atmosphere lights, and sky lighting. 

The `Env. Light Mixer` panel can be found in the `Window` menu of the editor.

## More on Geometry Brushes
Geometry brushes using the BSP (Binary Space Partitioning) approach are good for quickly creating level geometry. Unreal offers a number of basic shapes that can be easily edited to suit your level design needs.

### Brush Editing
Basic brushes can be edited using the Brush Editing Mode. This mode provides a small number of options for creating or modifying brushes. We'll look at editing vertices, extruding faces, drawing polygons with the pen tool.

### Creating Static Meshes from Brushes
Brushes come with a higher performance cost, so their use in a final game should be limited, especially if you use multiple instances of a single brush. You can replace these with static meshes created in 3D modeling software or convert your brushes to static meshes within the Unreal Editor. 

_Important: You will no longer be able to edit the brush after converting it. You may want to make a duplicate?_

To do this:
- Select your brush and navigate to `Brush Settings` in its Details panel.
- In the Advanced subheading, click the `Create Static Mesh` button and save it in your project folder with the prefix `SM_`.

#### Where's my collider?!
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/setting-up-collisions-with-static-meshes-in-unreal-engine/)
Converting a brush into a static mesh removes the colliders, but they are easy to replace.

To do this:
- Right-click on the static mesh and select `Edit SM_NameOfMesh`, which will launch the Mesh Editor window.
- From here you have many options for adding colliders to the static mesh in the `Collision` menu.
- Having trouble generating a mesh: Set the `Collision Complexity` under `Collision` to `Use Complex Collision as Simple`

## Adding a Player Character
To add Starter Content to your project, open the Content Browser and click on the `+ Add` button. From there, select `Add Feature or Content Pack` and select the `Third Person` (or `First Person`) Blueprint.

### What is a Blueprint?
A Blueprint (or Blueprint Class), is an asset that allows content creators to easily add functionality on top of existing gameplay classes. These essentially define a new class or type of Actor which can then be placed into maps as instances that behave like any other type of Actor.

### Third Person Starter Content Blueprints
- Adds a `ThirdPerson` folder to your project
- Most important are the `BP_ThirdPersonCharacter` and `BP_ThirdPersonGameMode` Blueprints in the `Blueprints` folder.

### Setting the Game Mode
To use a playable actor (pawn) in your game, the Game Mode needs to be set to match a Game Mode Blueprint which manages things like setting the playable Character and defining player input.

- Click the `Settings` button in the top right corner of the editor window and select `Project Settings`.
- Select `Maps and Modes` from under the `Project` heading in the Project Settings panel.
- Under `Default Modes`, set `Default Game Mode` to `BP_ThirdPersonGameMode` using the drop down menu.
- This will set up the properties for `Selected GameMode` to use the third person Starter Content. 

## Player Start Actor
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/player-start-actor-in-unreal-engine/)

This actor indicates a location where the player character will spawn and what direction it will face in the level. It can be found under the `Basic` heading in the `Place Actors Panel`.

## Importing FBX static meshes
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/importing-assets-directly-into-unreal-engine/) and [here](https://docs.unrealengine.com/5.2/en-US/fbx-static-mesh-pipeline-in-unreal-engine/).

The FBX export process and its setting will be a little different depending on the 3D modeling tool you use. Some helpful resources, in case you are stuck:
- Maya workflow documentation [here](https://docs.unrealengine.com/5.2/en-US/fbx-material-pipeline-in-unreal-engine/)
- Blender workflow documentation [here](https://www.youtube.com/watch?v=BBYIw23sFyU) (The quick way is fine for simple tasks)

Tips:
- Create a folder in the Content Browser and then import the asset into it using the `+ Add` button.
- Expect to rebuild your materials with the Material Editor in Unreal. The FBX material pipeline does not support the transfer of settings.
- Name your asset with a `SM_` prefix.
- Name your materials with a `M_` prefix

# Homework

## Blockout Exploration
_A blockout, or greybox, is a rough draft level built with simple shapes, but without details or refined art assets. The goal of a blockout is to prototype, test, and adjust the fundamental spatial relationships of a level._

For this assignment, you will be creating a blockout of a small environment that is explored by a player. This can be based on a singular real space or a composite of details from several real spaces.

This must include:
- Level geometry created using additive and subtractive brushes.
- One instance of geometry brush converted to a static mesh with a collider.
- At least one imported FBX static mesh.
- All visible surfaces need to have basic materials.
- Third person or First person character actor from Starter Content.
- Basic moodboard with photographic imagery of the space as reference materials for your work.

Do not use:
- Animated characters
- Interactive elements

### Important: What to turn in, where, and when

For this assignment, you will turn in:
- Unreal project
- Exported image of your reference moodboard

I sent out a link to the shared Google Drive folder to your MICA email last week. __Please have all work uploaded before the start of class next week (09/25).__

#### Reminder: Zip your files before uploading
Please zip your work folder and name it `yourname_week4_uew.zip` before uploading it. Otherwise, the files may become corrupted in the process.

# Upcoming events

## Animation & Game Design Community Get Together

Where: Brown 215

When: Wednesday, 2:15-3:30

## GameScape @ Artscape

Where: Joe Squared on North Ave

When: Sat & Sun, 12-5

Reach out to Melanie (mstegman@mica.edu) if you're interested in participating!
