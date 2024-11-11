# Creating User Interfaces

## Landscape Tools
The Landscape system inside of Unreal Engine is a collection of tools that allow you to create expansive outdoor environments.

Unreal's Documentation on the Landscape Editing Mode can be found [here](https://docs.unrealengine.com/5.4/en-US/editing-landscapes-in-unreal-engine/)

### How to access the tools
The Layout Mode tools can be accessed from the Modes dropdown menu in the Toolbar.

### Landscape Editor's Modes
There are three modes to the Landscape tools:
- Manage: Used to create new landscapes and modify the components of existing landscapes.
- Sculpt: Used to shape the landscape by manipulating the height of the terrain in different ways
- Paint: Used to apply weighted landscape materials to the terrain

### Demo Goals
Due to our abbreviated class, we will split our demo into two parts over the next two weeks. This week we'll focus on:
- Working with splines
- Adding grass and foliage
- Adding assets from Quixel Bridge or Fab (fingers crossed!)


### Landscape Splines

#### Adding Splines
Create a new Landscape Edit Layer and then right click it to select Reserve for Splines.

Manipulating splines:
- To add a new spline control point, Ctrl + click
- Transform tools can be used to move and rotate spline control points
- Dragging control point tangents are used to manipulate the curves
- The width of a spline segment can be set using the Half Width property


### Adding Landscape Grass

#### Creating Landscape Grass Type
The Landscape Grass Type asset is used to define the grass in your landscape. To create it, right click in Content Drawer, then select Foliage > Landscape Grass Type

#### Material nodes:
- Landscape Grass Output
- Landscape Layer Sample (Name the same as your target Layer)

### Adding Foliage
Any foliage you add can be seen in the Foliage panel. Refreshing the panel will update the list.

You can also add your own actors and static meshes with the `+ Foliage button`

#### Overview of tools
- Paint (Click and drag to add, Shift + click to erase)
- Lasso
- Single (Paint one at a time. Shortcut: i + click while painting)

__A video of today's demo will be uploaded by Wednesday morning.__

# Homework

## Complete Landscape Demo
Complete the homework from last week, adding the following:
- Material grass.
- Foliage added with the Foliage Tool.
- At least one landscape spline.
- Additional: You are also welcome to add other Static Mesh actors and lights to the level. 

Remember, there should be two levels in a loop:
- A start screen with button that opens second level.
- A main level with a goal that takes the player back to the start screen.


### Important: What to turn in, where, and when
Add a new folder to your root folder in the class drive called `lastname_firstname_landscape_study`. In this folder, add the following by the start of class next week (11/18):

- The Unreal project. Make sure to include the _entire_ project folder and _all_ of its files! 
- 3 high quality screenshots from UE5 which shows different views of your lit and textured map. _Don't forget to toggle Game View to remove the XYZ orientation widget._



__Bring this in-progress UE project to class next week as a jumping off point for further discussion on working with the Landscape Tools & Foliage Brushes.__

## Upcoming Opportunities

### Tronster Hartley (Firaxis) Talk & Pizza this  Thursday(11/14)!
Tronster will be visiting us on Thursday, 11/14 to give a talk in Dolphin on the 2nd Floor at 3:15pm. __There will also be pizza!__

_Tronster Hartley is a seasoned game developer with experience building video games for PCs, mobile devices, Facebook, and major gaming consoles. For the past 16 years, he has been a Senior Software Developer and Team Lead at Firaxis Games in Sparks, MD. He has led UX and UI teams for acclaimed titles such as Civilization VI and XCOM: Enemy Unknown. Currently, he is heading the UX and UI team for Civilization VII._

_In his spare time, Tronster actively promotes the video game industry, especially around Baltimore. He occasionally teaches as an adjunct professor at UMBC or UBalt. As the chair and a founding member of Baltimore's International Game Developers Association (IGDA) chapter, he helps foster the local game development community. He also created the MAGFest Indie Videogame Showcase, featured annually at the MAGFest convention in Washington, DC._
