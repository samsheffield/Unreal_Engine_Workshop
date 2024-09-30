# WELCOME BACK

## Using First Person Character Controller
- Starting from the template picker.
- Adding to a pre-existing project (Content Drawer > Add Feature or Content Pack...)
- Review: modifying basic interactivity blueprints to work with this character controller blueprints.

## Exporting Static Meshes
Static meshes can be easily exported from your project for further editing in Blender/Maya, or to use as scale reference. 

To export a satic mesh, select it in the Content Drawer, and then right-click to choose Asset Actions > Export.

## Importing FBX Static Meshes
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/importing-assets-directly-into-unreal-engine/) and [here](https://docs.unrealengine.com/5.4/en-US/fbx-static-mesh-pipeline-in-unreal-engine/).

### FBX Export Settings
The FBX export process and its setting will be a little different depending on the 3D modeling tool you use. Some helpful resources, in case you are stuck:
- Maya workflow overview [here](https://www.youtube.com/watch?v=jPABrxe81yc)
- Blender workflow overview [here](https://www.youtube.com/watch?v=FsV3ZUxmWLo&t=1s).

### Basic Import Workflow
There are two choices for importing FBX models:
- 1. Drag the FBX file directly into the Content Drawer.
- 2. Right Click on the Content Drawer and choose Import to...

### FBX Import Options
Once you start to import a file the FBX Import Options window will appear with various options that will direct the process. Many of these can be ignored, but here are some important options to be aware of.

#### Mesh Options
- Make sure Skeletal Mesh is _unchecked_ (this is for rigged animated meshes)
- Generate Missing Collision can stay checked (though it usually creates rather complex colliders that need to be fixed/replaced)
- Advanced: Combine Meshes (Check this if you have exported a static mesh that actually consists of many multiple meshes)

#### Material Options
- Material Import Method: Choose Generate new Materials
- Advanced: Invert Normal Maps (Check this if your imported Normal Map appears inverted. This can also be done in the Texture Editor)

#### Manage Files
- Move your files Material and Texture files to an appropriate folder.
- Name your asset with a `SM_` prefix.
- Name your materials with a `M_` prefix
- Textures are named with a `T_` prefix. Use an appropriate suffix for different maps. For example, Base Color (Diffuse) textures would use `_D` and Normal Maps would use `_N`. Refer to [this style guide](https://github.com/Allar/ue5-style-guide?tab=readme-ov-file#anc-textures) for more specifics.

### Other Tips:
- Create a folder in the Content Drawer and then import the asset into it using the `+ Add` button.
- Expect to rebuild your materials with the Material Editor in Unreal. The FBX material pipeline does not support the transfer of settings.
- Warnings: Sometimes you will see warnings, but they are often not critical. The most common is a Smoothing Groups warning which can be supressed by setting Smoothing Groups under your FBX Export settings.
- Normal Maps look inverted? Once imported, the normal map can be edited by double clicking on it. In the Texture Editor, search for Flip Green Channel in the Details panel.

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

## Working with Post Process Volumes
Documentation [here](https://docs.unrealengine.com/5.4/en-US/post-process-effects-in-unreal-engine/)

Post-processing effects enable artists and designers to define the overall look and feel of the scene through a combined selection of properties and features that affect coloring, tonemapping, lighting, and more. See the link above for exhaustive documentation on the kinds of effects available.

A Post Process Volume can be added to a Level to access these features. Multiple volumes can be placed to define the look of a specific area, or it can be set to affect the entire scene.

#### Post Process Volume Settings
The Post Process Volume Settings are specific settings for this placed volume and how it interacts with the scene and with any other Post Process Volumes it may overlap with. For example, you can toggle the `Infinite Extent` property to make this Post Process Volume affect everywhere in the scene, or leave it unchecked to have it affect only a certain area. When Volumes overlap, you can control how they interact with one another to blend from one to another, which is useful when you have radically different looks between them.

- __Priority__ - Specifies the priority of this volume. In the case of overlapping volumes, the one with the highest priority overrides the lower priority ones. The order is undefined if two or more overlapping volumes have the same priority.
- __Blend Radius__ - Sets the radius (in world units) around the volume that is used for blending. For example, when walking into a volume, the look can be different than that outside of the volume. The blend radius creates a transitional area around the volume.
- __Blend Weight__ - The amount of influence the volume's properties have. A value of 1 has full effect, while a value of 0 has no effect.

### Important! Default Post Processing
Unreal Engine uses some default post processing settings, even if you don't have a placed Post Process Volume in your Level. These default post process settings can be found and configured in the Project Settings in the `Rendering > Default Settings` section. It's often a good idea to disable these if you want to start with a clean slate.

# Homework

## Begin Open Exploration Project 1 (Due 10/21)
The project description can be found [here](project1.md)

### This week:
1. Find people to work with if you want to collaborate
2. Determine what you might want to make with the skill set you currently have
3. Prepare a [preliminary planning document](preliminaryprojectplanning.md)
4. Begin creating a moodboard (or moodboards) that establishes critical references and inspiration for your work.
5. Begin sketching and producing concepts for your spaces.


### Important: What to turn in, where, and when
Add a new folder to your root folder in the class drive called `lastname_firstname_project1`. In this folder, add the following by the start of class next week (09/16):

- 3 high quality screenshots from UE5 which shows different views of your greyboxed map or prototyping. _Don't forget to toggle Game View to remove the XYZ orientation widget._
- A copy of your planning document with your ideas, goals, and questions about the level. (See link above.)
- A copy of your planning sketches (those used for ideation or laying out a level).
- A link to a research material moodboard. _For Milanote, choose to Invite editors with a link and then share that with me in a text document._

