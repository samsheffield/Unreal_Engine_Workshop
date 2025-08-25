# W E L C O M E ! !
So excited to welcome you all back. Today, we'll meet as a group to...
- Say hello! (Who are you? How have you been? What are you excited/nervous about this semester?)
- Discuss this class and set expectations (Syllabus review)
- Tour Unreal Engine 5.6
- Talk about greyboxing

## This semester...
We're going to...
1. Have fun trying out an exciting new tool together (and swapping our steps and missteps along the way).
2. Explore strategies for building 3D interactive environments in Unreal Engine 5.
3. Build a solid foundation of technical know-how you can keep growing as confident Unreal Engine beginners!

## Getting to know Unreal Engine 5.6
We'll spend some time today getting to know the UE5 editor and general workflow.
- Become familiar with the basic operations and layout of the Unreal Editor.
- Begin working with Actors to create level geometry.
- Make some basic materials using the Material Editor.


## Unreal Engine 5.6 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation). It's rather good and organized topically. For the next couple of weeks we'll be focusing on content from the [Understanding the Basics](https://dev.epicgames.com/documentation/en-us/unreal-engine/understanding-the-basics-of-unreal-engine?application_version=5.6) section.

## Working with the Level Editor
Documentation links [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-editor-interface?application_version=5.6) and [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/level-editor-in-unreal-engine?application_version=5.6)
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
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/content-browser-interface-in-unreal-engine?application_version=5.6)
- Add assets from Starter Content
- Organization
- Pinning to screen

## Actors
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/actors-and-geometry-in-unreal-engine?application_version=5.6)
- How to add actors
- Common actor types (Static meshes, Brushes, Lights)
- Manipulating actors (translate/move, rotate, scale)
- Grouping actors (grouping and ungrouping, locking and unlocking)

### Static Meshes
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/static-mesh-actors-in-unreal-engine?application_version=5.6)
- Adding static meshes from the Content Browser
- Replacing static meshes

## Material Editor
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-material-editor-user-guide?application_version=5.6)
- Quick look at the Material Editor
- Main Material Node
- Create a simple solid color material


## Bonus Materials 

### Player Start Actor
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/player-start-actor-in-unreal-engine?application_version=5.6)

This actor indicates a location where the player character will spawn and what direction it will face in the level. It can be found under the `Basic` heading in the `Place Actors Panel`.


### Set default level in editor
- Project Settings > Project > Maps & Modes > Default Maps (Choose your map)

### How to create screenshots
- Viewport top right Perspective menu > High Resolution Screenshot

### Toggling Game View
- Press G to toggle. Hides all UI. Good for screenshots


## Greyboxing/Blockout Phase
A greybox/blockout is a rough prototype of a level built using simple 3D shapes and lacking in detail or detailed art assets. Blockouts are used to prototype and test foundational shapes and spatial relationships within a level.

_Fun Fact! Hideo Kojima designed levels for the original Metal Gear games using Lego and a camcorder ([image](https://drive.google.com/file/d/1wMhL1pLNk-Nfu0Se969zkQy9LjFYNPV6/view?usp=sharing))._

Great example of a greyboxed level: Brian Baker's Docks map for Modern Warfare ([image](https://drive.google.com/file/d/1o_7KrvE8u0GcXJwyWko69weKkgFLNBUW/view?usp=sharing)  ([original link](https://x.com/JrBakerChee/status/1182384066881916928/photo/1))


### Typical Level Design Workflow

#### Prototyping 
It’s very difficult to design a space for interaction if you don’t actually know what happens there! In games, these spaces are called _levels_ (or maps), and the actions players perform repeatedly are called _mechanics_. So, before any level design takes place, designers and developers prototype mechanics to figure out what players can do in the game, and, ideally, why those actions are fun.

In this phase, designers often make a quick sandbox level, even before building a real one, to test out mechanics and share key info with teammates, like how big the player is or how high and far they can jump.

Examples:
- [Splatoon Tofu Prototype](https://www.youtube.com/watch?v=0IJMXW0_dcU)
- [Zelda Windwaker Prototyping](https://drive.google.com/file/d/1F08JFpdc7LdWYHm5JQ0cOqF-MYKv4F3u/view?usp=sharing)


#### Ideation/Sketching/Research 
Before jumping into the level editor, designers first establish their ideas and goals for a level: What kind of experience do they want the player to have? What references can they gather to support that vision?

The first step is often to make written lists of goals and ideas, along with specific details or elements that might be included. This is also a great time to jot down any open questions about the level. This planning can happen on paper, in a text document, or in a spreadsheet.


Examples:
- [Internal planning board for Last of Us](https://drive.google.com/file/d/1fyRjoy9apU49u55gzCsubVY0743CHnEx/view?usp=sharing)
- Layout sketch
- Moodboard

After the initial ideas are in place, designers move on to sketching layouts and collecting references. Reference materials help inform design choices and give the level a sense of place. Moodboards are especially useful for organizing references and showing the patterns and relationships between them.

#### Greyboxing/Blockout
Finally, it’s time to open the level editor! At this stage, designers begin establishing spatial relationships relative to the controllable character. These “greyboxes” or “blockouts” are fast, rough 3D layouts made with simple shapes and little to no detail. They go through many revisions before settling.

#### Scripting
Interactive experiences like games require programming or scripting to make things happen. Once the level’s flow is established through blockouts, interactive elements are added. This step also usually goes through several rounds of iteration.

- Uncharted 4 Level Blockout Comparison ([link](https://www.youtube.com/watch?v=1SnMfyV5hXM))

#### Art & Lighting Passes
Only after the design becomes more certain do lighting, visual detail, and environment art get added. This is known as an _art pass_, and there are typically many across a project.

It’s often tempting to jump to this step and start making things beautiful right away, but doing so too early is risky. If art assets are added before the design is locked down, you may feel stuck with problems that are too expensive to fix later!

#### Case Study
For more insights into the level design process, check out:
- This writeup from Michael Barclay on his work as a level designer for Last of Us Part II ([link](http://www.mikebarclay.co.uk/blocktober-2020/)).
- The Level Design Book's Pre-production section ([link](https://book.leveldesignbook.com/process/preproduction)).



# Homework

__There are two assignments for the following two weeks:__
1. Class folder setup
2. Greybox study

## Set up class Picasso folder
Create a folder for all work submissions in the class drive on the Picasso file server named *Lastname_Firstname_GMD265*. 

Instructions on connecting to the Picasso file server can be found [here](https://www.mica.edu/campus-resources/technology/software/file-storage-servers/). 

_Note: It is slightly more complicated to do from off-campus, so I'd recommend getting things set up first while on-campus._

## Week 1 Homework: Level Design Study (Due 09/08)

### Assignment Details
__Design and block out a small playable level in Unreal Engine, focusing on level design principles rather than polished art.__ 

Use only basic shapes and the assets included in the First Person Template (Variant: None) folders in the Content Browser.

This exercise is about planning, experimenting with spatial relationships, and creating a playable space using greyboxing techniques.  

> **Assignment Goal:** Practice thinking like a level designer by turning ideas into playable spaces using simple geometry.


## Important Steps

1. **Document Your Ideas**  
   - Write down goals for your level. _What are you trying to accomplish?_
   - Include questions and ideas about how the space should feel and function.  

2. **Sketch Your Layout**  
   - Plan your level structure, marking any points of interest and how you imagine a player moving through the space.  
   - Sketches can be digital or on paper.  
   - *Note: Unreal Engine is not a sketching tool; this step is purely planning.*  

3. **Set Up Base Mechanics**  
   - Use the First Person Template (Variant: None) for player controls and interaction.  
   - Do not use alternative project templates or mechanics outside of what is included. 

4. **Greybox Your Level**  
   - Use basic shapes from the Place Actors panel as well as the static meshes included in the Meshes folder to block out your level.  
   - You may also use the Blueprint Actors from the Interactables folder to create a sense of progression to your space.  
   - Pay attention to player scale in all areas.   
   - Focus on spatial relationships, movement, and flow, not visual polish.  

5. **Apply Basic Materials**  
   - Assign simple materials (colors, basic shading) created with the Material Editor to distinguish objects, floors, and key gameplay areas.  
   - Do not use textures for this assignment.  

6. **Iterate and Experiment**  
   - Test your level frequently in Play Mode.  
   - Adjust scale, layout, and flow as needed.  


## Deliverables

Create a new folder in your Picasso class drive folder named:  
**Lastname_Firstname_GMD265_01**

By the start of next class, add the following:

1. **Screenshots** – 3 high-quality images from UE5 showing different views of your greyboxed map. Don’t forget to toggle **Game View** to hide the XYZ orientation widget (Hint: G key).  
2. **Planning Document** – A digital copy of your document with your ideas, goals, and questions about the level.  
3. **Level Layout Sketch(es)** – A digital copy of your sketches.  
4. **Unreal Engine Project Folder** - Make sure to include the entire folder and not just the ueproject file.


## Optional, but recommended
1. Join the MGL Discord (if you aren't already there). 

- [Here's the invitation link](https://discord.gg/hpGgwpX8sQ).
- You will need to visit the #welcome-and-rules channel to view the code of conduct and click the star emote to unlock the rest of the server.
- Make sure your server nickname is representative of your name in this class (and presumably outside of this class!) _How?_ https://support.discord.com/hc/en-us/articles/219070107-Server-Nicknames

2. Make sure to talk with me about any questions you might have heading into the semester. In particular, let me know if you have any questions regarding hardware or software.

