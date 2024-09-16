# Notes on Materials and the Material Editor

### Texture assets
Documentation [here](https://docs.unrealengine.com/5.4/en-US/textures-in-unreal-engine/)

Textures are image assets that are primarily used in Materials. UE5 supports a very broad set of image types including bmp, jpg, pg, psd, tga, and tif files. Use power of two sizes when possible, such as 32, 64, 128, 2048. UE5 provides performance benefits when using these sizes.

#### Importing textures 
Import textures using the `Import` button in the Content Drawer and organize in a folder.

#### Checking/editing texture assets
The Texture Asset Editor is a standalone window where you can view and edit Texture Assets. You can launch this editor by double clicking on a texture in the Content Drawer. This is a good tool for quickly tweaking your assets or specifying the type (for example, a normal map).

### Working with Texture Assets in the Material Editor
__TextureSample node__ - Outputs the color value(s) from a texture. (Documentation [here](https://docs.unrealengine.com/5.4/en-US/texture-material-expressions-in-unreal-engine/?utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#texturesample))

- Locate a 2D texture asset in the Details panel or create by dragging in an asset from the Content Drawer to the Material Graph.
- Connect the RGB outlet to `Base Color`.


### Other useful Material Editor nodes
- __Multiply__ - Takes two inputs, multiplies them together, and outputs the result. Documentation [here](https://docs.unrealengine.com/5.4/en-US/math-material-expressions-in-unreal-engine/?utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#multiply)
- __textureCoordinate__ - Outputs UV texture coordinates allowing materials to use different UV channels and specify tiling. Documentation [here](https://docs.unrealengine.com/5.4/en-US/coordinates-material-expressions-in-unreal-engine/?utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#texturecoordinate)
- __appendVector__ - This is used to create a 2 Vector Constant from two Constants. Documentation [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/math-material-expressions-in-unreal-engine?application_version=5.4&utm_source=editor&utm_medium=docs&utm_campaign=rightclick_matnode#appendvector)

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

## Emissive Materials
Documenttion [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/using-the-emissive-material-input-in-unreal-engine)

Emissive Materials provide an easy and effective way of creating an impression that a surface is glowing or casting light without using any of the standard Light Types.

Emissive Materials are created by using a Multiply node to inputting values higher than 1.0 into the Emissive Color input on the Main Material Node. This pushes the Material into the High-Dynamic Range (HDR), producing a bloom type of visual effect.

### Shading Model: Lit vs Unlit
- Use Unlit if your material does not need to interact with a level's lighting. Example: Surface of a light bulb.
- Use Lit if you need to use any of the other inputs of the Main Material Node. Example: A machine's panel with lights on it.

## Material Instancing
Documentation [here](https://docs.unrealengine.com/5.4/en-US/creating-and-using-material-instances-in-unreal-engine/)

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


What does UV mean?
u is x axis
v is y axis

What is a Normal Map?