# Landscape Tools & Blueprint Movement

## Reminder: External Hard Drive
I have two external hard drives that you can use to submit classwork each week if you are struggling with online storage caps. Please keep things organized.


## Today:
- Review homework
- Continue introduction to the Landscape Tools (2/2)

## Review Homework
Please set up your homework on your computers and find at least 3 other people to share with. I'll be making the rounds as well.


## Landscape Tools (2/2)
The Landscape system inside of Unreal Engine is a collection of tools that allow you to create expansive outdoor environments.

Unreal's Documentation on the Landscape Editing Mode can be found [here](https://docs.unrealengine.com/5.2/en-US/editing-landscapes-in-unreal-engine/)

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
- Creating holes in landscape
- Adding grass and foliage
- Adding assets from Quixel Bridge


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

### Working with Quixel Bridge

#### Opening Quixel Bridge
- Window > Quixel Bridge
- You will need to log in using your Epic Games linked account

#### Adding assets
- Navigate to your selected asset, choose the quality, and then click the Download button (sometimes there is a delay).
- Once downloaded, click the + Add button to add it to your project.


## Moving Actors with Blueprints
Blueprint Timelines can be used to create movement in different ways.

### Timeline

#### Some important things about Timelines
- To open a Timeline, double click it
- To create a Timeline Track, press the + Track button and choose the type
- The name of the track is exposed as an output pin of the Timeline.
- The overall length of a timeline is set in the toolbar.
- The Timeline toolbar has a few useful buttons displayed as icons:
    - Use Last Keyframe: When enabled, the last keyframe will be used.
    - AutoPlay: Eliminates the need to connect the Timeline node to BeginPlay.
    - Loop: Will allow Timeline to loop
- Shift + Click to add new keyframes
- Curves can be adjusted by first right-clicking on a keyframe and selecting Auto. Then drag tangents to alter curves.

#### Setting the Play Rate
Sometimes you'll want to set the timeline's duration outside of the Timeline node. To do this:
- Get the variable reference to the Timeline
- Use the Set Play Rate node
- Using a variable that divides 1 will set an overall rate in seconds 

#### Important nodes used in demo:
- Lerp (Vector)
- Set Relative Location
- Set Play Rate
- Add Timeline

### Moving an Actor along a spline
A Blueprint Spline Component is a path for you to define and use positional data. 

You can use it to move Actors (or other Components) around the world, or place a series of Actors (or other Components) along the spline. They are fully editable in the Blueprint Viewport and in the Level Editor, with the ability to add/remove/duplicate Spline Points, change their tangent types, and even animate them on tick.

#### Spline component
A spline component is used to create a spline in the level. Once the Blueprint Instance is added to the level you can manipulate the spline in the following ways:
- Add spline nodes: Select last spline point and drag while holding the Alt key
- Move and rotate spline points using usual tools.
- Drag spline point segment tangents to adjust curves.
- To create a closed loop, select the BP Instance's Spline component and check the Closed Loop box.
- Easily select points in the Spline component's Selected Points category.


#### Construction Script
The Construction Script runs when an instance of a Blueprint Class is created. This does not wait until BeginPlay.

#### Important nodes used in demo:
- Timeline
- Get Spline Length
- Lerp (Float)
- Get Location at Distance Along Spline
- Get Rotation at Distance Along Spline
- Set Actor Transform
- Get Location at Spline Point and Set Actor Location (Both of these are in the Construction Script)

## Landscape 

# Homework

## Thanksgiving
Take a break! See you next week.

## Open Exploration Project 2 (Due 12/11)
The project description can be found [here](project2.md)

### Decide what you want to work on for Open Exploration Project 2
1. Find people to work with if you want to collaborate.
2. Determine what you might want to make with the skill sets you currently have and the remaining things we will cover over the remaining weeks.