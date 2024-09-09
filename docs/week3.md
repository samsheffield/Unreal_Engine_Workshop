# Getting familiar with the Unreal Editor
Welcome back Today, we'll meet as a group to...
- Get familiar with the basic operations and layout of the Unreal Editor.
- Begin working with Actors to create level geometry.


## Unreal Engine 5.4 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://docs.unrealengine.com/5.4/en-US/). It's rather good and organized topically. For the next couple of weeks we'll be focusing on content from the [Understanding the Basics](https://docs.unrealengine.com/5.4/en-US/understanding-the-basics-of-unreal-engine/) section.

## Working with the Level Editor
Documentation links [here](https://docs.unrealengine.com/5.4/en-US/unreal-editor-interface/) and [here](https://docs.unrealengine.com/5.2/en-US/level-editor-in-unreal-engine/)
- Basic overview (Viewport, Toolbars, Content Browser, Outliner, Details)
- Select Editing Mode
- Navigating the Viewport
- Modes: Immersive mode (F11), Game (G), Orthographic views
- Working with Actors
- Creating and editing Materials (basics)
- Creating and saving Levels (maps)
- Geometry brushes and mesh modeling
- Saving screenshots
- Saving your work!

## Working with the Content Browser
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/content-browser-interface-in-unreal-engine/)
- Add assets from Starter Content
- Organization
- Pinning to screen

## Actors
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/actors-and-geometry-in-unreal-engine/)
- How to add actors
- Common actor types (Static meshes, Brushes, Lights)
- Manipulating actors (translate/move, rotate, scale)
- Grouping actors (grouping and ungrouping, locking and unlocking)

### Static Meshes
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/static-mesh-actors-in-unreal-engine/)
- Adding static meshes from the Content Browser
- Replacing static meshes

## Material Editor
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/unreal-engine-material-editor-user-guide/)
- Quick look at the Material Editor
- Main Material Node
- Create a simple solid color material
- _More Material Editor next week!_

### Brushes
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/geometry-brush-actors-in-unreal-engine)
- Static mesh vs geometry brush
- Additive vs Subtractive modes
- Applying materials (select all surfaces with SHIFT + J or SHIFT + B)

### Modeling Mode
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/getting-started-with-modeling-mode)
- Creating basic shapes
- Extruding polygons


## Levels
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/working-with-levels-in-unreal-engine/)
- Creating new levels
- Working with level templates (Starter Content)
- Starting from scratch (Empty template)

## Bonus Materials 

### Disabling Default Postprocessing
Unreal Engine has a neat visual effects enabled by default. Sometimes these can be _a bit much._ To quickly disable these:
- Project Settings > Engine > Rendering > Default Settings (Can also search for rendering or default settings).


### Set default level in editor
- Project Settings > Project > Maps & Modes > Default Maps (Choose your map)

### How to create screenshots
- Viewport top left menu > High Resolution Screenshot

### Toggling Game View
- Press G to toggle. Hides all UI. Good for screenshots


## Greyboxing/Blockout Phase
A greybox/blockout is a rough prototype of a level built using simple 3D shapes and lacking in detail or detailed art assets. Blockouts are used to prototype and test foundational shapes and spatial relationships within a level.

_Fun Fact! Hideo Kojima designed levels for the original Metal Gear games using Lego and a camcorder ([image](/docs/images/Kojima_MG1_Lego.png))._

Great example of a greyboxed level: Brian Baker's Docks map for Modern Warfare ([image](/docs/assets/images/COD_Docks_Blockout.jpg))  ([original link](https://x.com/JrBakerChee/status/1182384066881916928/photo/1))


### Typical Level Design Workflow

#### Prototyping 
It is not possible to successfully design levels for something interactive if you don't know how it works! In games, the things that we do repeatedly are called _mechanics_. So, before any level designing occurs, devlopers figure out what a player can do in their game by prototyping mechanics.

During this phase, it's common to create a small _sandbox_ level to test mechanics and also communicate to other teammates important  metrics such as how big a player character is, high/far they can jump, etc.

Examples:
- [Splatoon Tofu Prototype](https://www.youtube.com/watch?v=0IJMXW0_dcU)
- [Zelda Windwaker Prototyping](/docs/assets/images/zelda_windwaker_prototyping.jpg)


#### Ideation/Sketching/Research 
Before firing up the level editing tools, level editors start out by establishing their ideas and goals for a level, figuring out what kind of experience they want a player to have, and gathering lots of reference materials.

The first step is often just creating written lists of any goals and ideas the designer has, along with specific details/elements that might be included in the level. This is also a good point for the designer to jot down any questions they might have about the level. This process might take place on paper, a text document, or spreadsheet.


Examples:
- [Internal planning board for Last of Us](/docs/assets/images/Naughty_Dog_Planning_Board.png)
- Layout sketch
- Moodboard


After ideas are in place, designers begin sketching level layouts and gathering reference materials. Regardless of ference materials help inform a designer's decisions and give a level a _sense of place_. Moodboards are great tools for collecting and organizing reference materials as they help convey patterns and relationships between the individual sources.

#### Greyboxing/Blockout
Finally! Time to start establishing the spatial relationships in the level editor, relative to the controllable character. As mentioned above, these are fast and rough 3D levels using simple shapes and lacking detail. This phase typically goes through many stages of revision.

#### Scripting
Interactive experiences such as games require some programming/scripting to make things happen. Once the level's flow is established from blocking things out, interactive elements are added to the level. This phase also goes through many phases of revision.

- Uncharted 4 Level Blockout Comparison ([link](https://www.youtube.com/watch?v=1SnMfyV5hXM))

#### Art & Lighting Passes
Only once things become more certain in a level's design are lighting and visual detail/environment art added. This process is referred to as an _art pass_. There are typically many, many art passes in a project.

It's often tempting to want to skip to this step and make the world beautiful, but this is a very risky move. If art assets are implemented too early, developers can often feel stuck with problems that might persist because undoing or removing art assets would be too costly.

#### Case Study
For more information on the level design process, I would recommend:
- This writeup from Michael Barclay on his work as a level designer for Last of Us Part II ([link](http://www.mikebarclay.co.uk/blocktober-2020/)).
- The Level Design Book's Pre-production section ([link](https://book.leveldesignbook.com/process/preproduction)).



# Homework

## Week 3 Homework: Greybox Study

_Note: This is the first part of a two week assignment. Please only focus on the planning, research, and blockout this week._


Over the next two weeks, you will create a study of a small interior or exterior space with one point of interest using Unreal Engine's Level Editor. You are encouraged to experiment, explore, and make a mess. Try things out and don't be afraid to make mistakes!

This week will be planning and greyboxing. Next week, you will flesh out the study and add lighting.

Criteria:
- Start by creating a text document with your initial ideas, goals, and questions for the level.
- Produce at least one sketch laying out your level. _This can be on paper or using an digital drawing software._
- Create a moodboard using Milanote (or equivalent) with at least 10 reference images conveying elements, details, and feeling you want in your level.
- Use the Third Person Template as a base. _These are your mechanics._
- Greybox level geometry using basic shape actors, geometry brushes, or static meshes created with the modeling tools. _Do not create any 3D assets outside of UE5 this week._ 
- Level geometry must be made relative to scale with the player character.
- All visible surfaces need to have basic materials applied. _No textures this week._
- The map does not need to be a 1:1 recreation of a real space, but you must use reference materials to inform the spatial relationships in your map.

### Important: What to turn in, where, and when
Add a new folder to your root folder in the class drive called `lastname_firstname_greybox_study`. In this folder, add the following by the start of class next week(09/16):

- 3 high quality screenshots from UE5 which shows different views of your greyboxed map. _Don't forget to toggle Game View to remove the XYZ orientation widget._
- A copy of your planning document with your ideas, goals, and questions about the level.
- A copy of your level layout sketch(es).
- A link to your research material moodboard. _For Milanote, choose to Invite editors with a link and then share that with me in a text document._

**You do not need to turn in the UE project files this week.**
