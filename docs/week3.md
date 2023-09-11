# Getting familiar with the Unreal Editor
Welcome back Today, we'll meet as a group to...
- Get familiar with the basic operations and layout of the Unreal Editor

## How would you like notes from our demos?
I'm currently planning to provide weekly demo notes in the form of a recorded video (uploaded by Tuesday, following our class meeting). 

I can also provide written notes (cheatsheets) for specific subjects where it might be helpful, but will otherwise try to direct you to Unreal Engine's documentation directly when I can. 

Let me know if you have any preferences and I'll do my best to accommodate requests.


## Unreal Engine 5.2 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://docs.unrealengine.com/5.2/en-US/). It's rather good and organized topically. For the next couple of weeks we'll be focusing on content from the [Understanding the Basics](https://docs.unrealengine.com/5.2/en-US/understanding-the-basics-of-unreal-engine/) section.

## Working with the Level Editor
Documentation links [here](https://docs.unrealengine.com/5.2/en-US/unreal-editor-interface/) and [here](https://docs.unrealengine.com/5.2/en-US/level-editor-in-unreal-engine/)
- Basic overview (Viewport, Toolbars, Content Browser, Outliner, Details)
- Select Editing Mode
- Navigating the Viewport (3 ways: Mouse, WASD, Maya)
- Modes: Immersive mode (F11), Game (G), Orthographic views
- Bookmarks (saving and recalling)
- Saving screenshots
- Saving your work!

## Working with the Content Browser
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/content-browser-interface-in-unreal-engine/)
- Add assets from Starter Content
- Organization
- Pinning to screen

## Actors
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/actors-and-geometry-in-unreal-engine/)
- How to add actors
- Common actor types (Static meshes, Brushes, Lights)
- Manipulating actors (translate/move, rotate, scale)
- Grouping actors (grouping and ungrouping, locking and unlocking)

### Static Meshes
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/static-mesh-actors-in-unreal-engine/)
- Adding static meshes from the Content Browser
- Replacing static meshes

### Brushes
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/geometry-brush-actors-in-unreal-engine)
- Static mesh vs geometry brush
- Additive vs Subtractive modes
- Hollow geometry
- Applying materials (select all surfaces with SHIFT + J or SHIFT + B)

## Material Editor
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/unreal-engine-material-editor-user-guide/)
- Quick look at the Material Editor
- Main Material Node
- Create a simple solid color material
- _More Material Editor next week!_

## Lights
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/light-types-and-their-mobility-in-unreal-engine/)
- Quick look at realtime lighting with Lumen
- Realtime vs baked lighting
- Common types of light (point, spot, directional, rect, sky lights)

## Levels
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/working-with-levels-in-unreal-engine/)
- Creating new levels
- Working with level templates (Starter Content)
- Starting from scratch (Empty template)

## Bonus Materials 

### Disabling Auto Exposure effect
Unreal Engine has a neat effect which is intended to simulate the way one's eyes adjust to light when moving from an exterior to interior space. To quickly disable this:
- Add a Post Process Volume Actor (put it anywhere in your level)
- Check the `Infinite Extent (Unbound)` box in Post Process Volume Settings.
- Check the `MinEV100` and `MaxEV100` boxes in `Exposure` and set their values both to 1.

### Change the position of the sun
The sun in the sky is dynamic! To move it use `CTRL + L` while dragging your mouse.

### Starting from scratch
The empty template is great to work with when you need a clean slate to work from, but seeing a black screen in the Viewport can be a little confusing at first. At minimum, you probably want:
- A Directional light actor
- A SkyAtmosphere actor (from Visual Effects)
- An ExponentialHeightFog actor (from Visual Effects)
- Optional: A Skylight actor
- Optional: A box brush to create a ground surface (from Geometry)

# Homework

## Warm-up exploration
Create a small interior or exterior space using only built-in tools and Starter Content assets. You are encouraged to experiment, explore, and make a mess. Try things out!

This must include:
- Most level geometry created using additive and subtractive brushes
- One instance of geometry brush set to hollow
- At least one static mesh (can be either basic shapes or assets from Starter Content)
- At least 3 light sources
- All visible surfaces need to have materials
- At least one basic material that you create using the Material Editor
- Optional: use of materials from Starter Content 

Do not use:
- Imported assets (_We'll do this next week!_)
- Character controllers
- Interactive elements

### Important: What to turn in, where, and when
I will send out a link to the shared Google Drive folder to your MICA email during class today. __Please have all work uploaded before the start of class next week (09/18).__

#### Create a folder
Create a folder to submit your classwork into named `yourname_uew_f23`. This folder is only ofr submitting classwork and will be erased after the end of the semester, so please keep your own backup.

#### Zip your files before uploading
Please zip your Unreal project folder and name it `yourname_week3_uew.zip` before uploading it. Otherwise, the files may become corrupted in the process.
