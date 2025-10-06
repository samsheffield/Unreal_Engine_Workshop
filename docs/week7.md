# W E L C O M E ! !
So excited to welcome you all back. Today, we'll meet as a group to discuss...
- Landscape Tools introduction
- Landscape Materials basics
- Spline-based movement (Blueprints)


## Video Demos
Weekly demo videos can be found on our class Canvas Welcome page. I will have new videos posted no later than Wednesday evening most weeks.

_Need a specific demo?_ Let me know!


## Reminder: Unreal Engine 5.6 Documentation
In addition to what we cover in class each week, the greatest place you can look for additional information is [the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation). Check it out!

---

## Unreal Engine 5: Landscape Tools

The Landscape System in Unreal Engine 5 is a powerful set of tools for creating large-scale, natural outdoor environments such as mountains, valleys, and fields.

Unreal’s official documentation on the Landscape Editing Mode can be found here:  
[Landscape Editing in Unreal Engine](https://docs.unrealengine.com/5.0/en-US/landscape-editing-in-unreal-engine/)

---

### Accessing the Landscape Tools

You can access the Landscape Mode from the Modes dropdown menu in the Toolbar.

---

### Landscape Editor Modes

The Landscape Editor has three main modes:

1. Manage – Create or resize landscapes and manage components (add or remove sections).  
2. Sculpt – Shape the terrain by raising, lowering, or smoothing the heightmap.  
3. Paint – Apply landscape materials (textures) using painted weight layers.

---

### Creating a New Landscape Asset

1. Open Landscape Mode from the Toolbar.  
2. Under the Manage tab, click Create New.  
3. Adjust Section Size and Component Count to set your overall terrain dimensions.  
4. Click Create to generate the landscape.  
5. Save it as a Landscape Asset in your Content Drawer.

Tips for creating new landscapes:
- Start with a smaller landscape size for prototyping; you can expand it later.  
- Keep overall resolution under control (e.g., 2017x2017 or smaller) to maintain performance.  
- If importing a heightmap, make sure it uses a 16-bit grayscale format for accurate elevation data.

---

### Editing a Landscape Asset with the Manage Tab

The Manage tab allows you to modify or reorganize an existing landscape after it has been created.

Common tasks include:

- Add or Remove Components – Expand or shrink the playable area by selecting Add or Delete and clicking in the viewport.  
- Change Landscape Size – Adjust the overall width or height of the landscape by changing component counts.  
- Move Landscape – Use the Move tool to reposition the entire landscape within your level.  
- Change Section Settings – Modify component or section sizes to adjust the density and level of detail.  
- Visibility Tool – Hide or reveal specific regions of the landscape for optimization or level design purposes.  

Tips:
- When adding new components, they will appear using the current heightmap or as flat sections.  
- Always save after making structural changes to prevent breaking references in your level.  
- Keep landscape dimensions in powers of two for best performance and compatibility with LODs.

---

### Sculpting the Landscape

Use the Sculpt Mode to modify terrain height and shape.

Six most important sculpt tools:

1. Sculpt Tool – Raises or lowers terrain (using Shift key).  
2. Smooth Tool – Softens rough edges or sharp changes in elevation.  
3. Flatten Tool – Levels terrain to a uniform height (platforms and plateaus).  
4. Ramp Tool – Creates smooth inclines between two points.  
5. Erosion Tools – Simulates natural erosion for realistic landscapes.
6. Erase Tool - Return Landscape to starting height.

Tips:
- Experiment with brush falloff for smoother elevation shifts.
- Adjust brush size with [ and ] keys.  
- Use low brush strength (0.05–0.15) for finer control.  
- __Use reference materials!__

---

### Landscape Splines

Splines can be used to create paths, roads, rivers, or other curved geometry that conforms to the landscape.

Steps to use Splines:

1. Create a new Landscape Edit Layer.  
2. Right-click the new layer and select Reserve for Splines.  
3. Use Ctrl + Click in the viewport to add spline control points.  
4. Move or rotate control points with standard transform tools.  
5. Adjust the tangent handles to refine curve shape.  
6. Change spline width using the Half Width property.

---

### Landscape Material Basics

Landscape Materials define the textures and blending of surfaces (for example, grass, dirt, or rock).

To create one:

- Create a Material in the Content Drawer.  
- Use Landscape Layer Blend nodes to define texture layers (Grass, Rock, Dirt, etc.).  
- Use Landscape Layer Sample nodes to reference these layers in other nodes.  
- Apply the material to your landscape in the Details panel.  

Useful Material Nodes:

- Landscape Layer Blend – Combines multiple texture layers.  
- Landscape Layer Sample – Samples a specific named layer (must match Paint Layer name).  
- Landscape Grass Output – Spawns grass or foliage automatically using material rules.


_We'll look at adding more foliage next week._

---

### Spline Movement

The Spline Component can be combined with a Timeline to move actors smoothly along a path—useful for camera paths, vehicles, or guided movement.

Useful Nodes:

- Get Spline Length – Returns the total length of the spline.  
- Get Location at Distance Along Spline – Returns a position at a specific distance (set Coordinate Space to World).  
- Get Rotation at Distance Along Spline – Gets rotation/orientation along the spline (set Coordinate Space to World).  
- Lerp (Float) – Smoothly interpolates between two values over time.  
- Set Actor Transform – Updates position and rotation each frame.

In a Construction Script:

- Use Set Actor Location + Get Location at Spline Point (World Space).  
- Adjust index or distance to position the actor along the spline dynamically.

---

## Week 7 Homework: Landscape Study – First Pass (Due 10/20)

### Assignment Details
This week you will begin working with Unreal Engine’s Landscape Tools to create a small outdoor environment, designed to lead a player toward a destination.   

You will create **two versions** of the same scene in two differnt levels:
1. A **Blockout Level (Greybox)** used to establish basic proportions and scale.
2. A **Refined Level** where placeholder geometry is replaced with sculpted landscape details, improved lighting, and early materials.

You may use your own 3D assets or download items from the Fab storefront to supplement your scene. _If you download assets from anywhere else, make sure to provide proper attribution credits in a text file which accompanies the project._

### Criteria
- Create a new Unreal Engine project for this assignment.  
- Build a small landscape using the Landscape Tools.  
- Sculpt terrain that guides the player toward a destination or focal point.  
- Create **two levels**:
  - **Level 1: Blockout (Greybox)**  
    - Use simple shapes and a rough landscape to establish scale and player movement.  
    - Focus on sightlines, height relationships, and overall layout.  
  - **Level 2: Refined Version**  
    - Duplicate your blockout level.  
    - Replace placeholder geometry with refined meshes and landscape sculpting.  
    - Begin adding lighting and simple materials to define tone and atmosphere.  
- Find **2–3 reference images** that inspire the composition or mood of your scene.  
- Focus on designing a **“beautiful corner”**: a small area or viewpoint that feels intentional and well-composed.  
- Use light, color, and form to subtly direct the player’s movement.  
- Avoid high realism; experiment with composition and tool use instead.  

### Deliverables
Create a new folder in your class drive named:  
`YourName_GMD265_07`

In this folder, include:

- **Unreal Project Folder:** The complete Unreal Engine project (not just the .uproject file).  
- **Two Levels:**
  - `Level_Blockout` – Simple geometry and landscape for player scale testing.  
  - `Level_Refined` – Updated version with improved sculpting, lighting, and early material setup.  
- **Reference Images:** 2–3 images that inspired your space or guided your design decisions.  
- **Screenshots:** At least 3 images showing:
  - The blockout version with basic geometry.  
  - The refined version showing terrain improvements.  
  - An example of the player’s perspective or path through the space.

### Tips and Reminders
- Focus on a small, contained area—avoid large open worlds.  
- Use the **[** and **]** keys to adjust landscape brush size.  
- Keep brush strength low (around 0.05–0.15) for fine control.  
- Don’t over-polish; this is a first pass to learn landscape tools.  
- Use lighting, color, and shape to draw attention naturally toward your destination.  
- Next class, you’ll add **Spline Paths** and **Foliage Brushes** to continue developing this scene.
