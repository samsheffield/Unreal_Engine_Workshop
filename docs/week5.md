# Material Editor, Working with Textures, Material Instances Volumes, Post Processing 

## Review Blockout Explorations
Let's spend some time taking a look at everyone's weekend explorations.

## Volumes
Documentation link [here](https://docs.unrealengine.com/5.2/en-US/volume-actors-in-unreal-engine/)

Volumes are three-dimensional support Actors, generally used to detect when certain Actor types have entered a specific area and trigger something in response. Volumes sometimes have built-in effects of their own (either in code or Blueprints).

You can use Volumes to implement effects and behaviors like:

- Causing damage to the player or other Actors inside the Volume.
- Blocking certain Actors from entering the Volume, acting as a collision surface.
- Changing something in the environment (for example, opening a door) when an Actor enters the Volume.
- Changing the lighting or visibility in a Level.

#### Placing a Volume
You can add a volume into your Level using the Place Actors panel. Once placed in the Level, use the Details panel to access all the available properties and features.

### Blocking Volumes
Blocking Volumes block other Actors from passing through them. You can use Blocking Volumes instead of collision surfaces on Static Meshes, particularly in the case of walls in structures. This can cause scenes to operate more predictably, since physical objects won't interact with small details like bumps on the floor and walls. It can also improve performance by reducing the cost of physics simulation.

### Post Process Volume
Documentation [here](https://docs.unrealengine.com/5.2/en-US/post-process-effects-in-unreal-engine/)

Post-processing effects enable artists and designers to define the overall look and feel of the scene through a combined selection of properties and features that affect coloring, tonemapping, lighting, and more. See the link above for exhaustive documentation on the kinds of effects available.

A Post Process Volume can be added to a Level to access these features. Multiple volumes can be placed to define the look of a specific area, or it can be set to affect the entire scene.

#### Post Process Volume Settings
The Post Process Volume Settings are specific settings for this placed volume and how it interacts with the scene and with any other Post Process Volumes it may overlap with. For example, you can toggle the `Infinite Extent` property to make this Post Process Volume affect everywhere in the scene, or leave it unchecked to have it affect only a certain area. When Volumes overlap, you can control how they interact with one another to blend from one to another, which is useful when you have radically different looks between them.

- __Priority__ - Specifies the priority of this volume. In the case of overlapping volumes, the one with the highest priority overrides the lower priority ones. The order is undefined if two or more overlapping volumes have the same priority.
- __Blend Radius__ - Sets the radius (in world units) around the volume that is used for blending. For example, when walking into a volume, the look can be different than that outside of the volume. The blend radius creates a transitional area around the volume.
- __Blend Weight__ - The amount of influence the volume's properties have. A value of 1 has full effect, while a value of 0 has no effect.

### Something new to me! Default Post Processing
Unreal Engine uses some default post processing settings, even if you don't have a placed Post Process Volume in your Level. These default post process settings can be found and configured in the Project Settings in the `Rendering > Default Settings` section.


## A little deeper into the Material Editor
- Working with Textures
- Tiling UVs
- Converting nodes to Parameters
- Creating Material Instances

### Texture assets
Documentation [here](https://docs.unrealengine.com/5.2/en-US/textures-in-unreal-engine/)

Textures are image assets that are primarily used in Materials. UE5 supports a very broad set of image types including bmp, jpg, pg, psd, tga, and tif files. Use power of two sizes when possible, such as 32, 64, 128, 2048. UE5 provides performance benefits when using these sizes.

#### Importing textures 
Import textures using the `Import` button in the Content Drawer and organize in a folder.

#### Checking/editing texture assets
The Texture Asset Editor is a standalone window where you can view and edit Texture Assets. You can launch this editor by double clicking on a texture in the Content Drawer. This is a good tool for quickly tweaking your assets or specifying the type (for example, a normal map).

### Working with Texture Assets in the Material Editor
__TextureSample node__ - Outputs the color value(s) from a texture. (Documentation [here](https://docs.unrealengine.com/5.2/en-US/texture-material-expressions-in-unreal-engine/?utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#texturesample))

- Locate a 2D texture asset in the Details panel or create by dragging in an asset from the Content Drawer to the Material Graph.
- Connect the RGB outlet to `Base Color`.


### Other useful Material Editor nodes
- __Multiply__ - Takes two inputs, multiplies them together, and outputs the result. Documentation [here](https://docs.unrealengine.com/5.2/en-US/math-material-expressions-in-unreal-engine/?utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#multiply)
- __textureCoordinate__ - Outputs UV texture coordinates allowing materials to use different UV channels and specify tiling. Documentation [here](https://docs.unrealengine.com/5.2/en-US/coordinates-material-expressions-in-unreal-engine/?utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#texturecoordinate)
- __appendVector__ - This is used to create a 2 Vector Constant from two Constants. Documentation [here]()

### Working with Displacement maps
Displacement mapping is a texturing method that uses a displacement of points on the textured surface to create dimensional effects.

UE5 does not support displacement maps in the material editor but it's easy to implement them via the `Modeling Mode` tools.

#### Modeling Mode
Modeling Mode is a set of tools to create and modify Static Meshes. It's powerful and we'll discuss it this semester. For now, we're going to focus on only one detail: vertex displacement.

__Important Note 1: If you are working with a basic static mesh shape actor, you won't be able to apply your changes. You can easily recreate these shapes in Modeling Mode though.__

### Applying a Displacement Map
- Switch to `Modeling Mode` in the mode selection drop-down menu in the top left corner of the editor window.
- Select the static mesh in the editor window.
- From the `Deform` heading choose `Displce`.
- Under the Modeling pane, change `Displacement Type` under the `Options` heading to `Texture2D Map` and then locate your displacement map from the drop-down menu.
- Modify options (see below) and choose `Accept` when done

Critical options:
- __Displace Intensity__ - How strong is the effect
- __Subdivisions__ - How much detail is used to create the effect

__Important Note 2: Choosing Accept will make permanent changes. You will not be able to undo this afterwards.__

## Material Instancing
Documentation [here](https://docs.unrealengine.com/5.2/en-US/creating-and-using-material-instances-in-unreal-engine/)

Material instancing is a way to create a parent Material that you can use as a base to make a wide variety of different looking children (Material instances).

To achieve this flexibility, Material instancing uses a concept called inheritance: the properties of the parent Material are passed to its children. Properties that are designated as parameters in the parent Material are exposed to artists in the Material Instance Editor.

### Creating a Material Instance
- First, create a base material to use as a parent for your Material Instances
- In the Content Drawer, right click and select `Material > Material Instance`
- Name the new Material Instance `MI_NameOfBaseMaterial`.
- Double click on the Material Instance to launch the Material Instance Editor and set `General > Parent` to the base material in the details panel.

#### Converting Material Editor nodes to Parameters
Many material expression nodes can be converted to parameters. To do this, right click on the node and select `Convert to Parameter`. Then give the parameter a unique name.

You can edit the way the parameter appears in any Material Instance in the Details panel and manipulate it in the Parameters panel.

#### Editing Material Instances
A Material Instance's parameters can be edited using the Material Instance Editor.


## Adding Components to Actors
You can add Actors to other Actors to create more complex, reusable Actors using the Details panel.

At the top of the panel, all of the Components of the selected Actor are displayed. Clicking the `+ Add` button allows you to add additional Actors.

Selecting the Component from this list will allow you to manipulate it in the Viewport.


### Converting an Actor to a Blueprint Class
Sometimes you might also want an instance of an Actor that you've made to reuse in your Levels. This is helpful if you've made a lot of adjustments or added components to an Actor.

- Select the Actor and click the Blueprint icon (next to + Add) in the Details panel. 
- Create `New Subclass`
- Name the new Blueprint with the prefix `BP_`
- Select the folder you want to create it into and click `Select`

## Open Exploration Project 1 (Due 10/23)
The project description can be found [here](project1.md)

# Homework

## Mood Exploration
For this assignment, you will be creating a textured blockout of a small environment that is explored by a player that evokes a particular mood. References for this assignment can be based on real or fictional sources.

This must include:
- Playable character
- Blocking volumes which limit the player's movement to a specific area
- Use of lighting
- At least two post processing volumes (one should be set to Infinite Unbound)
- Use of textured materials
- Two or more Material Instances that are derived from the same parent material
- A duplicated instance of a Blueprint class created from an Actor with a component

Do not use:
- Animated characters
- Interactive elements

### Important: What to turn in, where, and when

For this assignment, you will turn in:
- Unreal project
- Exported image of your reference moodboard

I sent out a link to the shared Google Drive folder to your MICA email last week. __Please have all work uploaded before the start of class next week (10/02).__

#### Reminder: Zip your files before uploading
Please zip your work folder and name it `yourname_week5_uew.zip` before uploading it. Otherwise, the files may become corrupted in the process.


## Begin Open Exploration Project 1
1. Find people to work with if you want to collaborate
2. Determine what you might want to make with the skill set you currently have
3. Prepare a [preliminary planning document](preliminaryprojectplanning.md)
4. Begin creating a moodboard (or moodboards) that establishes critical references and inspiration for your work.
5. Begin sketching and producing concepts for your spaces.


### Important: What to turn in, where, and when

For this assignment, you will turn in:
- Preliminary planning document

I sent out a link to the shared Google Drive folder to your MICA email last week. Please create a new folder in Project 1 for you (or your team) and [transfer the ownership to me](https://support.google.com/drive/answer/2494892?hl=en&co=GENIE.Platform%3DDesktop). __Please have all work uploaded before the start of class next week (10/02).__

