# Lighting in the Unreal Editor
Welcome back Today, we'll meet as a group to...
- Review blockouts/greyboxing
- Recap/expand conversation on Static Mesh modeling tools and BSP brushes
- Work with textures and maps in the Material Editor
- Discuss realtime lighting in Unreal Engine 5 (Lumen)
- *Hopefully* introduce Quixel Bridge integration


## Review blockouts/greyboxing
- Meet in small groups to share planning materials and blocked out levels.
- Have volunteers share out to the class

## More on Modeling Tools & BSP Brushes

### BSP Geometry Brushes
- To prevent light leaks, Unreal recommends Wall Thickness of at least 10 cm when using Hollow geometry. 
- To successfully subtract a brush: Brush Settings > Advanced > Sorting Order (Set Subtractive Geometry to Last).
- Brushes can be converted to Static Meshes for reuse: Brush Settings > Advanced > Create Static Mesh. Save with a "SM_" prefix. _Important: Once converted you cna not edit it as a Geometry Brush any longer!_
- Reminder: Select all faces of a brush using Shift + B.

#### Where's my collider?!
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/setting-up-collisions-with-static-meshes-in-unreal-engine/)

Converting a brush into a static mesh removes the colliders, but they are easy to replace.

To do this:
- Right-click on the static mesh and select `Edit SM_NameOfMesh`, which will launch the Mesh Editor window.
- From here you have many options for adding colliders to the static mesh in the `Collision` menu.
- Having trouble generating a mesh: Set the `Collision Complexity` under `Collision` to `Use Complex Collision as Simple`

### Modeling Tools
- Create: Consider using shapes from here instead of the Basic Shapes Place Actors tab since they provide a lot of flexibility.
- _GENERATED folder: When you create a static mesh it is placed in a folder relative to your current level. Feel free to rename and move it elsewhere.
- Changing pivot points: (XForm > Edit Pivot)
- To reshape a Static Mesh: (Model > Polygroup Edit)
- Projecting a UV to a surface: (UV > Project UV)

### Temporarily set Pivot Offset
- Alt + Middle Mouse click on new pivot point. This will stay active for one following action. 
- You can also set this to be persistent by Right clicking > Pivot > Set as Pivot Offset and reset it with Pivot > Reset Pivot Offset.

## A little deeper into the Material Editor
- Working with Textures
- Tiling and Offsetting UVs
- Scalar Parameters
- Emissive Materials
- Creating Material Instances

This week's notes on materials can be found [here](week4_materialnotes.md)

## Lighting in Unreal

We will be focusing on the sophisticated realtime lighting ssytem in UE5 called Lumen. There is a non-realtime type of lighting typically used in game engines referred to as _baked lighting_. This produces a static texture for your level geometry and can produce beautiful results with limited overhead. The downsides are that these are not affected by realtime lighting changes and that the process is both fussy and time-consuming.

### What is Lumen?
Lumen is Unreal Engine 5's fully dynamic global illumination and reflections system that is designed with next-generation and high end computing platforms in mind. It is the default global illumination and reflections system for Unreal Engine 5.

## Common Types of Lights
Documentation link [here](https://docs.unrealengine.com/5.4/en-US/light-types-and-their-mobility-in-unreal-engine/)

- Ambient Lighting (Sky Lights): Help establish shapes from background. Omnidirectional. Global impact.
- Directional Lights & Sun: Help define shapes through a distincion with shadow. One direction. Global impact.
- Spot Lights & Rect Lights: Directional light used to highlight shapes. One direction. Local impact.
- Point Lights: Help draw attention to shapes.

## Direct vs Indirect Lighting
Direct lighting involves the actual shining of a light at a surface. Indirect lighting is the effect of the light bouncing off of one surface onto another. Together, these are referred to as Global Illumination.

[Example](https://drive.google.com/file/d/1sKPAsSCBzdWPOdgCiWvKrHSZ-AlAVDM1/view?usp=sharing) of 3 types (unlit, direct, and indirect + direct).

## Three Point Lighting
Three Point Lighting is a practical lighting theory used in cinema and photography. This theory utilizes three _types_ of lighting to light a subject. This can be applied to games, though it is challenged by the mobile nature of many games' camera.

Three Point Lighting consists of:
- Key light: The key light is the main light in a scene.
- Fill light: Used to control the amount of contrast. Typically less intense than Key light.
- Rim light: Sometimes called back light or hair light. Used to separate subject from the background.Video games often use a fresnel effect for this.

A [standard setup](https://steamuserimages-a.akamaihd.net/ugc/578979510333219336/FD338BA9529937014E2FB7E9AC0DBA03374E071F/) might look like this.

[Examples from film (Does three point lighting suck?)](https://lightingpixels.blogspot.com/2013/01/tutorials-does-three-point-lighting-suck.html)

## How to set up lights in Unreal
- Setting up environmental lights
- Setting up point, spot, and rect lights
- Most common properties (exposure, color, temperature, source/attenuation radius)

### Addressing common issues with Lumen
How to deal with splotchy lighting (AKA "Lumen Crawling") with a Post Processing Volume.

In low lighting situations, Lumen can often produce an effect similar to light reflecting off of the surface of a swimming pool. This is sometimes referred to as "Lumen Crawling". This can sometimes be tricky to completely eliminate, but it is possible to minimize the effect using the following approaches.

### Post-Processing Volumes
A Post-Procssing Volume is XXX. Post-Processing Volumes can have their effects limited to particular areas or applied everywhere on a level. These volumes are added through the Place Actors panel.

To extend the bounds of a volume infinitely, search for Infinite Extent in the Details panel for the volume and check the box.

### Fix 1: Increase the Final Gather Lighting Pass

Search for `Final Gather Quality` in a Post-Processing Volume's Details panel. Boost this number upwards until the effect is minimized. Note: this will have a dramatic impact on GPU usage, so use cautiously.

### Fix 2: Add more light and adjust exposure

The negative effect can be minimized by introducing more light into a space. Add lights or increase an existing light's Intensity property. To counter the brightness, set the `Exposure Compensation` property of a Pot-Processing Volume to a negative number.

## Working with Quixel Bridge
__Note: We should be all good to go on the lab computers with Quixel this week, but if not, we'll demo the process in class and you can use your home computers until we address any issues.__

### What is Quixel Megascans?

[Quixel Megascans](https://quixel.com/megascans) is a very large online library of high quality 3D scan assets that happens to be free for use in Unreal Engine. This is an excellent resource for realistic props and materials.

Unreal provides a tool to access this library called Quixel Bridge.

#### How to add Quixel Assets
- Right Click on the Content Drawer and choose `Add Quixel Content`.
- You will be asked to Log in or create a plan (Choose the free Unreal Engine option).
- Navigate to the content of your choice and choose the Download button (green arrow) to add it to your library, followed by the Add button to add it to your project (blue button).
- This content is added to a Megascans folder relative to your current level.


# Homework

## Week 4 Homework: Lighting Study

_Note: This is the second  part of a two week assignment. Please focus on lighting and texturing this week._


This week, you will continue developing your study of a small interior or exterior space with one point of interest by adding lighting, textured materials, and small props. Consider the mood or atmosphere of the space you are creating. You are encouraged to experiment, explore, and make a mess. Try things out and don't be afraid to make mistakes!

Criteria:
- Make any desired adjustments to your greyboxed level.
- Add basic types of lighting to your greyboxed level. At minimum, this should include a Directional Light, Point Light, and Spot Light/Rect Light.
- Consider adding emissive materials to actors which serve as a light source.
- Add a texture to at least one materials. _This will be an overall texture which gives more information about the type of surface. Do not get into UV unwrapping and detailed texture painting!_
- Add small props from Quixel's library. These should support, not distract from, your level geometry and help flesh out its sense of place.

### Important: What to turn in, where, and when
Upload this week's submissions to the `lastname_firstname_greybox_study` folder created last week. In this folder, add the following by the start of class next week (09/23):

- The Unreal project. Make sure to include the _entire_ project folder and _all_ of its files! 
- 3 high quality screenshots from UE5 which shows different views of your lit and textured map. _Don't forget to toggle Game View to remove the XYZ orientation widget._

# Game Design Events This Week

## Fall Student Show Reception on Thursday (09/19) from 3-5 pm
Check out some student games and prototypes this week in the Dolphin Gallery. There will be a catered reception on Thursday. Please stop by! 

## Game Night this Friday (09/20) on Dolphin 2nd Floor!
Come play some games and eat pizza. Everyone is welcome!