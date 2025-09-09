# W E L C O M E ! !
So excited to welcome you all back from the holiday. Today, we'll meet as a group to discuss...
- Realtime lighting in UE5
- More working with materials
- Post-processing effects

We'll also...
- Meet our TA
- Review your homework from week 1

## Video Demos
Weekly demo videos can be found on our class Canvas Welcome page. I will have new videos posted no later than Wednesday evening most weeks.

_Need a specific demo?_ Let me know!


## Reminder: Unreal Engine 5.6 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation). Check it out!


## Lighting in Unreal

### What is Lumen?
Lumen is Unreal Engine 5's fully dynamic global illumination and reflections system that is designed with next-generation and high end computing platforms in mind. It is the default global illumination and reflections system for Unreal Engine 5.

### Realtime Lighting
We will be focusing on the sophisticated realtime lighting system (Lumen) in UE5. There is a non-realtime type of lighting typically used in game engines referred to as _baked lighting_. This produces a static texture for your level geometry and can produce beautiful results with limited overhead. The downsides are that these are not affected by realtime lighting changes and that the process is both fussy and time-consuming.

## Common Types of Lights
Documentation link [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/light-types-and-their-mobility-in-unreal-engine?application_version=5.6)

- **Ambient Lighting (Sky Lights)**: Help establish shapes from background. Omnidirectional. Global impact.
- **Directional Lights & Sun**: Help define shapes through a distinction with shadow. One direction. Global impact.
- **Spot Lights & Rect Lights**: Directional light used to highlight shapes. One direction. Local impact.
- **Point Lights**: Help draw attention to shapes.

## Direct vs Indirect Lighting
Direct lighting involves the actual shining of a light at a surface. Indirect lighting is the effect of the light bouncing off of one surface onto another. Together, these are referred to as _Global Illumination_.

[Example](https://drive.google.com/file/d/1sKPAsSCBzdWPOdgCiWvKrHSZ-AlAVDM1/view?usp=sharing) of 3 types (unlit, direct, and indirect + direct).

## Three Point Lighting
Three Point Lighting is a practical lighting theory used in cinema and photography. This theory utilizes three _types_ of lighting to light a subject. This can be applied to games, though it is challenged by the mobile nature of many games' camera.

Three Point Lighting consists of:
- **Key light**: The key light is the main light in a scene.
- **Fill light**: Used to control the amount of contrast. Typically less intense than Key light.
- **Rim light**: Sometimes called back light or hair light. Used to separate subject from the background.Video games often use a fresnel effect for this.

A [standard setup](https://steamuserimages-a.akamaihd.net/ugc/578979510333219336/FD338BA9529937014E2FB7E9AC0DBA03374E071F/) might look like this.

[Examples from film (Does three point lighting suck?)](https://lightingpixels.blogspot.com/2013/01/tutorials-does-three-point-lighting-suck.html)

## How to set up lights in Unreal
- Setting up environmental lights
- Setting up point, spot, and rect lights
- Most common properties  in the Details panel (exposure, color, temperature, source/attenuation radius)

### Actor Mobility Settings
The Mobility setting controls whether an Actor can move or change in some way during gameplay. This primarily applies to Static Mesh Actors and Light Actors. It is located in the Actor's Details panel, under the Actor's Transform coordinates.

An Actor that supports this setting can have one of three mobility states:
- **Static**: Reserved for Actors that will not move or update in any way during gameplay. Ideal for structural or decorative meshes.
- **Stationary**: Reserved for Actors that can change during gameplay but not move. Stationary light actors can have their color or intensity changed or even being completely off.
- **Movable**: Reserved for Actors that need to be added, removed, or changed in some way during gameplay. **Movable lights support Lumen and cast dynamic shadows**.


### Addressing common issues with Lumen
How to deal with splotchy lighting (AKA "Lumen Crawling") with a Post Processing Volume.

In low lighting situations, Lumen can often produce an effect similar to light reflecting off of the surface of a swimming pool. This is sometimes referred to as "Lumen Crawling". This can sometimes be tricky to completely eliminate, but it is possible to minimize the effect using the following approaches.


### Possible fix: Add more light and adjust exposure

The negative effect can be minimized by introducing more light into a space. Add lights or increase an existing light's Intensity property. To counter the brightness, set the `Exposure Compensation` property of a Post-Processing Volume to a negative number.

## A little deeper into the Material Editor
- Working with Textures
- Tiling and Offsetting UVs
- Emissive Materials
- Transparent Materials
- The Fresnel effect
- Creating Parameters
- Creating Material Instances

**This week's notes on materials can be found** [**here**](week3_materialnotes.md).


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

## Class TA! Duncan Kelly!
Duncan will be here from 1-3pm during class and available for office hours in D200 (Game Lab) on Wednesday from 1-3pm.

Please do not reach out to Duncan for help outside of these times.


# Homework

# Week 3 Homework: Lighting & Atmosphere Study (Due 09/15)

## Assignment Details
__Using your Week 1 greyboxed environment, apply a second pass to your space by introducing lighting, textured materials, props, and post-processing volumes to establish a particular mood or feeling.__
 

**Assignment Goal:** This exercise is about learning how light, material, and atmosphere shape player experience. Practice using Unreal Engine’s real-time lighting, materials, and post-processing tools to create an environment that communicates a specific visual and emotional tone. 

---

## Important Steps

### Set Visual Goals
- Gather reference material (images, films, concept art, or other games) that capture the mood or feeling you want to achieve.  
- Write down a few notes about what atmosphere you’re aiming for (for example: creepy, inviting, warm, claustrophobic, surreal).  

### Refine Your Level
- Make any adjustments to your Week 1 greybox as needed to support your new visual direction.  
- Ensure your space still has a clear point of interest.  

### Lighting Pass
- Add basic types of lights to your level. At minimum, include:  
  - Directional Light (for sunlight or global ambient light).  
  - Point Lights for  distinguishing shapes.
  - Spot or Rect Lights for drawing focus.
- Experiment with intensity, color, and shadows.  
- Consider using emissive materials on objects to create diegetic light sources.  

### Materials and Textures
- Replace at least one of your simple materials with a textured material to suggest surface type (wood, stone, metal, concrete, etc.).  
- Do not worry about UV unwrapping or custom texture painting yet. Stick to simple overall surface treatments.  

### Post-Processing
- Add Post-Processing Volumes to experiment with atmosphere.  
- Consider using an Unbound Post-Processing Volume to create an overall effect.
- Try adjusting exposure, bloom, vignette, saturation, or contrast to reinforce your chosen mood.  

### Iterate and Experiment
- Test your level frequently in Play Mode.  
- Try multiple lighting and post-processing setups before settling on one.  
- Don’t be afraid to make a mess and try bold or unexpected choices.  

---

## Deliverables
Create a new folder in your Picasso class drive folder named:  
`Lastname_Firstname_GMD265_03`  

By the start of next class, add the following:  

1. **Screenshots** – 3–5 high-quality images from UE5 showing your lighting, materials, and post-processing results. Toggle *Game View* (press `G`) to hide the XYZ orientation widget.  
2. **Reference Material** – Include any images or other references that guided your visual goals.  
3. **Short Reflection** – Briefly explain your design intentions: what mood you aimed for, how you approached it, and what worked or didn’t. A paragraph or two in length will be plenty. 
4. **Unreal Engine Project Folder** – Include the full project folder (not just the `.uproject` file).  



## Optional, but recommended
1. Join the MGL Discord (if you aren't already there). 

- [Here's the invitation link](https://discord.gg/hpGgwpX8sQ).
- You will need to visit the #welcome-and-rules channel to view the code of conduct and click the star emote to unlock the rest of the server.
- Make sure your server nickname is representative of your name in this class (and presumably outside of this class!) _How?_ https://support.discord.com/hc/en-us/articles/219070107-Server-Nicknames

2. Make sure to talk with me about any questions you might have heading into the semester. In particular, let me know if you have any questions regarding hardware or software.

