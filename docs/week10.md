# Creating User Interfaces

## Unreal Motion Graphics (UMG) UI Designer
Unreal's documentation can be found [here](https://docs.unrealengine.com/5.4/en-US/umg-ui-designer-for-unreal-engine/).

The UMG is a visual system for creating user interfaces in the Unreal Editor.

Unreal's documentation can be found [here](https://docs.unrealengine.com/5.4/en-US/umg-ui-designer-for-unreal-engine/).

## Widgets
In User Interface terms, a widget it a component which enables a user to complete a function. The UMG uses widgets to create layout elements. These are contained in a `widget blueprint class`

Documentation [here](https://docs.unrealengine.com/5.4/en-US/creating-widgets-in-unreal-engine/).

## Widget Blueprint
This is where you design your layout

To create a widget blueprint:
- Right click on Content Drawer window.
- From User Interface select Widget Blueprint.
- Choose the option for User Widget.
- Save the blueprint class with a `WB_` prefix.

### Widget Blueprint Editor
The editor is broken into two primary modes:
- Designer tab: This is where you add and arrange layout widgets.
- Graph tab: This is where you can script logic for the widget blueprint.

#### Basic Editor Panels
- Palette: Contains the widget libraries available to the project. Widgets can be added to UI by dragging and dropping them from this panel.
- Hierarchy: Displays the widgets that belong to the UI and their relationship to one another. Similar to the Outliner in other editor views.
- Details: This provides access to a widget's properties.
- Editor Graph: This is where the UI its Blueprint is designed, depending on editor mode.

#### Root widget
Widget blueprints always contain a root widget. If selected in the Hierarchy, you can set the overall properties of the widget.

## UI Widgets
There are many widgets that can be added to a UI. Here are some of the widgets we will be looking at today:
- Canvas Panel
- Text
- Image
- Progress Bar

### Canvas panel
A canvas panel acts as a basic container for other layout elements. It should be the first thing you add and can be found in the Panels subheading in the Palette.



#### Anchors
Anchors are used to designate where a widget should drawn when a window changes size.This can be set manually by moving the anchor medallion or by choosing presets from a widget's Anchor dropdown menu.

#### Binding widgets
Widgets can be bound to the values of variables set in the Event Graph. Clicking on the visibility icon (an eye) next to a variable's name in the Event Graph will make it a public variable. Public variables can be used by other blueprint classes and expose the variable to the widget properties i the Details panel.

### Blueprint functions
There are many ways to organize your blueprint nodes so that they can take up less space in the Event Graph and be easily reused. We'll look at functions today, which are similar to Custom Events but are better suited for containing parts of your blueprint which you want to reuse.

Detailed information on Blueprint functions can be found [here](https://docs.unrealengine.com/5.4/en-US/functions-in-unreal-engine/)

# Homework

## UMG GUI Demo 2
This weekend, you'll be getting a headstart on our next topic of discussion- creating User Interfaces (UI). [Here is a video](https://youtu.be/bULo0uMeqWM?si=ras4GC2x30rzBqsO) demo which I've created to demonstrate the basics of UI creation in UE5.

## For next week
Follow along with my demo and create a new UE project which includes:
- A custom Game Mode Blueprint
    - Set this as the Default Game Mode in `Project Settings > Maps & Modes`.
    - This needs to be set up to use the BP_ThirdPersonCharacter as Default Pawn.
- A Widget Blueprint for UI
    - This should be set up to display an item count which we will update through interaction next week.
    - Include the following widgets: Canvas, Text
    - Don't forget to anchor the UI widgets
    - Import and use a custom font for the UI Text
- Blueprints for a "collectable" item
    - For now, the Blueprint's Actor should be destroyed using OnBeginOverlap
    - Next week, we'll keep count and reflect this in the UI

__Bring this in-progress UE project to class next week as a jumping off point for further discussion on how to update the UI in realtime.__