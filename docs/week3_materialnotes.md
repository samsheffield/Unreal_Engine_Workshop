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

## Emissive Materials
Documentation [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/using-the-emissive-material-input-in-unreal-engine)

Emissive Materials provide an easy and effective way of creating an impression that a surface is glowing or casting light without using any of the standard Light Types.

Emissive Materials are created by using a Multiply node to inputting values higher than 1.0 into the Emissive Color input on the Main Material Node. This pushes the Material into the High-Dynamic Range (HDR), producing a bloom type of visual effect.

### Shading Model: Lit vs Unlit
- Use Unlit if your material does not need to interact with a level's lighting. Example: Surface of a light bulb.
- Use Lit if you need to use any of the other inputs of the Main Material Node. Example: A machine's panel with lights on it.

## Material Instancing
Documentation [here](https://docs.unrealengine.com/5.4/en-US/creating-and-using-material-instances-in-unreal-engine/)

Material instancing is a way to create a parent Material that you can use as a base to make a wide variety of different looking children (Material instances).

To achieve this flexibility, Material instancing uses a concept called inheritance: the properties of the parent Material are passed to its children. Properties that are designated as parameters in the parent Material are exposed to artists in the Material Instance Editor.

### When to use a Material Instance?
A Material Instance calculates only once, prior to runtime. Although they remain constant throughout your game, they have a performance advantage of not requiring compilation.

For example: 

Your game has a variety of cars with different paint jobs whose colors will not change during gameplay, the best practice is to create a master Material representing the base aspects of car paint. You'd then create Material Instances to represent the variations for different types of car, such as different colors, levels of roughness, etc. 

### Creating a Material Instance
- First, create a base material to use as a parent for your Material Instances
- In the Content Drawer, right click on the material and select `Create Material Instance`
- Name the new Material Instance `MI_NameOfBaseMaterial`.

#### Converting Material Editor nodes to Parameters
Many material expression nodes can be converted to parameters. To do this, right click on the node and select `Convert to Parameter`. Then give the parameter a unique name.


#### Editing Material Instances
A Material Instance's parameters can be edited using the Material Instance Editor.
- Double click on the Material Instance to launch the Material Instance Editor.
- You can edit the way the parameter appears in any Material Instance in the Details panel under `Parameter Groups`. Depending on the type of parameter, it will appear in one of the Global Parameter Groups.