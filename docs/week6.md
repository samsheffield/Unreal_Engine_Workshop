# W E L C O M E ! !
So excited to welcome you all back. Today, we'll meet as a group to discuss...
- Importing static meshes from Blender/Maya/etc. (FBX files)
- Intro to UE5's static mesh modeling tools
- Keeping count and moving things with Blueprints (Functions and Custom Events)


## Video Demos
Weekly demo videos can be found on our class Canvas Welcome page. I will have new videos posted no later than Wednesday evening most weeks.

_Need a specific demo?_ Let me know!


## Reminder: Unreal Engine 5.6 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation). Check it out!

---

## Working with Static Meshes

### Importing FBX Assets
- Static meshes are non-animated 3D models (not skeletal meshes, which include animation data and rigging)
- Export from a Digital Content Creator (DCC) such as Maya, Blender, etc. as FBX format (do not use native file types)
- Import to the Content Browser by right-clicking and selecting Import to Content Browser
- The Import menu can be used to specify what is imported or fix small problems
- Check for colliders before importing
- Only use basic materials (textures are okay)
- Common import issues to check:
  - Scale consistency (Unreal Engine: 1 unit = 1 cm)
  - Pivot location (center vs base)
  - Z direction
  - Normals and smoothing groups

### General Recommendations for Static Mesh Complexity

Unreal Engine uses polygons (Tris) and will convert any imported quads used in modeling. Keep poly counts proportional to importance, putting detail where the player will notice. Experiment.

__Environment assets (props, furniture, small objects)__
- Usually 300–5,000 triangles depending on size and detail.

__Hero props (objects you see up close, weapons, vehicles, interactables)__
- Around 5,000–20,000 triangles.

__Background / filler assets__
- Keep these very low, often under 500–1,000 triangles.

---

### Nanite
Nanite is Unreal Engine 5’s system for rendering very high-poly 3D models in real time by automatically handling detail and performance without manual LODs.  

[Unreal Engine Documentation: Nanite Virtualized Geometry](https://dev.epicgames.com/documentation/en-us/unreal-engine/nanite-virtualized-geometry-in-unreal-engine?application_version=5.6)


#### How to Enable Nanite on an Imported Static Mesh

__Import your mesh__
- Import it as an FBX or other supported format  
- Place it in your Content Browser  

__Open the Static Mesh asset__
- Double-click your mesh in the Content Browser to open the Static Mesh Editor  

__Enable Nanite support__
- In the Details panel, under Nanite Settings, check the box labeled **Enable Nanite Support**  
- Click **Apply Changes**  

__Save and close__
- Once Nanite is enabled, save the mesh asset  

__Check in viewport__
- Place the mesh in your level  
- In the **Viewport → Nanite Visualization** menu, turn on views like *Triangles* or *Clusters* to confirm Nanite is active  


---

### Modeling Tools
- Very powerful toolset with functionality similar to DCC software
- Not a recommended replacement for Maya, Blender, or other DCC tools at this time
- Accessible in the Modeling Mode dropdown menu at the top left of the Viewport window
- Useful for common tasks:
   - Editing Static Meshes
  - Editing pivot points
  - Fixing normals
  - Splitting meshes
  - Projecting UVs
- Resources:
  - [Unreal Engine Documentation: Modeling Tools](https://dev.epicgames.com/documentation/en-us/unreal-engine/modeling-mode-in-unreal-engine?application_version=5.6)
  - [Unreal Engine 5 | Level Design | Greybox Entire Levels in Minutes](https://www.youtube.com/watch?v=heg8kGSMnZg)
  - [YouTube: 50 Tips and Tricks in Modeling Mode | Unreal Fest 2024](https://www.youtube.com/watch?v=xIMudHNX9JM)

---

## Blueprint Examples

### This week's concepts
- Variables: store and retrieve information (health, score, ammo, etc.)
- Custom events and functions: reusable logic blocks  
  - [Custom Events Documentation](https://docs.unrealengine.com/5.0/en-US/blueprints-custom-events-in-unreal-engine/)  
- Inheritance: blueprint classes can extend others  
  - [Inheritance Documentation](https://docs.unrealengine.com/5.0/en-US/blueprint-class-inheritance-in-unreal-engine/)  
- Communication between blueprints: references, casting, interfaces, or event dispatchers  
  - [Blueprint Communication Overview](https://docs.unrealengine.com/5.0/en-US/blueprint-communication-in-unreal-engine/)

### Examples
- Custom Event (Collectable Item)
  - Create a `CollectItem` custom event in your collectable blueprint  
  - Trigger it on overlap with the player character  
  - [Custom Events Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/custom-events-in-unreal-engine?application_version=5.5)
- Spawning Actors
  - Use `Spawn Actor from Class` to dynamically add actors into the world  
  - [Spawn Actor from Class Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Game/SpawnActorfromClass?application_version=5.6)  
- Timers and Loops
  - Use `Set Timer by Function Name` or `Set Timer by Event` to create repeating logic  
    - [Set Timer by Function Name Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Utilities/Time/SetTimerbyFunctionName)  
    - [Set Timer by Event Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Utilities/Time/SetTimerbyEvent)  
  - Use `Clear and Invalidate Timer` to stop it  
    - [Clear and Invalidate Timer by Handle Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Utilities/Time/ClearandInvalidateTimerbyHandle?application_version=5.6)  
- Timelines
  - Used to create timed events or smooth animations  
  - Example: move an object back and forth with a Timeline and a `Lerp (Vector)` node  
  - [Timelines Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/timelines-in-unreal-engine?application_version=5.0)  
  - [Lerp Node Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Math/Vector/Lerp_Vector?application_version=5.6)  


# Homework

## Week 6 Homework: Static Meshes and Blueprints (Due 10/06)

### Assignment Details
This week you will practice importing static meshes, making small adjustments with Unreal’s Modeling Tools, and scripting Blueprints that spawn and animate Actors. You will also create a simple collectable object that updates a variable on the First Person Character.

Your task is to import at least one custom static mesh from a DCC tool (Maya, Blender, etc.), adjust it with Modeling Tools, and use Blueprints to spawn an Actor that animates back and forth with a Timeline. You will also create a collectable Actor that increments a counter on the First Person Character when collected.

### Criteria
- Create a static mesh in the DCC of your choice (Not an animator? It does not need to be complex!) __Do not use an FBX which you find online.__
- Import a static mesh as an FBX and check for common issues
- Rebuild Materials in Unreal Engine
- Use Modeling Tools to make small mesh adjustments~~~~
- Spawn an Actor into the level at runtime
- Animate an Actor using a `Timeline` and `Lerp (Vector)`
- Create a collectable Actor with collision
- Communicate between Blueprints to increment a counter (using a variable) on the player Blueprint (It can Print String or do something like change level or destroy an actor)
- Organize and comment Blueprint logic clearly

### Deliverables
Create a new folder in your Picasso class drive folder named:
`YourName_GMD265_06`

In this folder, include:

- Unreal Project Folder: The complete project folder (not just the .uproject file)
- Screenshots: At least 3 images showing:
  1. A mesh edited with Modeling Tools
  2. A spawned Actor moving with a Timeline
  3. The collectable Actor and the counter increment on your First Person Character
- The original (non-FBX) 3D file created in your DCC

### Tips and Reminders
- This assignment does not need to be a cohesive environment
- Keep meshes simple; focus on process and workflow
- Use `Print String` to debug before finalizing logic
- Test your Blueprints often in Play Mode
- Keep it simple! This assignment should take no more than 5 hours (including modeling time!)
