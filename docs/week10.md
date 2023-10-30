# Intro to UMG UI Designer, Blueprint Functions

## Reminder: External Hard Drive
I have two external hard drives that you can use to submit classwork each week if you are struggling with online storage caps. Please keep things organized.

## Unreal Motion Graphics (UMG) UI Designer
Unreal's documentation can be found [here](https://docs.unrealengine.com/5.2/en-US/umg-ui-designer-for-unreal-engine/).

The UMG is a visual system for creating user interfaces in the Unreal Editor.

Unreal's documentation can be found [here](https://docs.unrealengine.com/5.2/en-US/umg-ui-designer-for-unreal-engine/).

### Widgets
In User Interface terms, a widget it a component which enables a user to complete a function. The UMG uses widgets to create layout elements. These are contained in a `widget blueprint class`

Documentation [here](https://docs.unrealengine.com/5.2/en-US/creating-widgets-in-unreal-engine/).

### Widget Blueprint
This is where you design your layout

To create a widget blueprint:
- Right click on Content Drawer window.
- From User Interface select Widget Blueprint.
- Choose the option for User Widget.
- Save the blueprint class with a `WBP_` prefix.

#### Editor
The editor is broken into two primary tabs:
- Designer tab: This is where you add and arrange layout elements.
- Event Graph tab: This is where you can script logic for the widget blueprint.

#### Root widget
Widget blueprints always contain a root widget. If selected in the Hierarchy, you can set the overall properties of the widget.

#### Canvas panel
A canvas panel acts as a basic container for other layout elements. It should be the first thing you add and can be found in the Panels subheading in the Palette.

#### Anchors
Anchors are used to designate where a widget should drawn when a window changes size.This can be set manually by moving the anchor medallion or by choosing presets from a widget's Anchor dropdown menu.

#### Binding widgets
Widgets can be bound to the values of variables set in the Event Graph. Clicking on the visibility icon (an eye) next to a variable's name in the Event Graph will make it a public variable. Public variables can be used by other blueprint classes and expose the variable to the widget properties i the Details panel.

### Blueprint functions
There are many ways to organize your blueprint nodes so that they can take up less space in the Event Graph and be easily reused. We'll look at functions today, which are similar to Custom Events but are better suited for containing parts of your blueprint which you want to reuse.

Detailed information on Blueprint functions can be found [here](https://docs.unrealengine.com/5.2/en-US/functions-in-unreal-engine/)

## Demo Video by Wednesday
This demo is going to demonstrate a number of interconnected things that are needed to implement a basic gameplay loop, so expect it to be quite involved. The video demo will be uploaded early on Wednesday.

# Homework

## Package your Open Exploration Project
You only need to create a package for your primary computer platform (Windows or MacOS). 

Onc packaged, test the application and then zip the entire build folder (Rename it from Windows or MacOS to _yourname_project1_uew_). Upload this to your online Drive folder or have it ready to transfer to the external drive next week.

### Small Game Loop
For this assignment, you will be creating a small complete game loop which goes from start screen to game level to end screen (and then loops back to start screen). You're welcome to use ths same mechanics that we introduced in-class today, but I want you to recreate the blueprints if you take that approach.

This must include:
- Start screen with a title and a button.
- Game level which has win and lose conditions. 
- An end screen selected by the win or lose condition which restarts the game after a small delay.

Important:
Do not add multiple levels in which it's necessary to carry a score from one to the next. We will discuss the GameInstance class next week, which is used for this kind of thing.


#### Important: What to turn in, where, and when
You can either upload the work to your class Drive folder (preferred) or transfer it to my external drive next week.

#### Zip your files before uploading
Please zip your Unreal project folder and name it `yourname_week10_uew.zip` before uploading it. Otherwise, the files may become corrupted in the process.