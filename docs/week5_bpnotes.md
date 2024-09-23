## What is a Blueprint?
Blueprint has more than one meaning in Unreal Engine.
1.  It's the name of the visual scripting language used in the Unreal Engine. 
2.  It's a type of complex game object created using the Blueprint language.

There are two main types of Blueprints: 
- Level Blueprint: Each Level has its own Level Blueprint (and only one).
- Blueprint Class.  These are used to create interactive objects which can be reused in any Level.

## Object Oriented Programming (OOP)
Blueprints are based on the principles of object-oriented programming (OOP). Some of the fundamental concepts are...

#### Classes
A class is a template for creating objects and providing its initial properties (variables or attributes) and behaviors (events or functions).

When creating a Blueprint, we are creating a new class that is used to create objects in the levels of a game. 

#### Instances
An object created from a class is also known as an instance of that class.

Instances are created with the same default values for their variables as  defined in the Blueprint Class. It is possible to mark a variable's
value as Instance Editable to change one instance's variable without affecting other instances.

#### Inheritance
Classes can inherit variables and functions from other classes. 

When creating a Blueprint, we choose its parent class. A Blueprint Class can only have one parent class (a superclass) but can have several child classes (subclasses).

## Creating a Blueprint
1. To create an empty Blueprint: Right click in the Content Drawer and select Blueprint Class. There are many Parent Classes to choose from. Select Actor.
2. To create a Blueprint from something in a level: Select the Actor and click the Convert to Blueprint Class button at the top of the Details panel (looks like three small rectangles).

### Naming Blueprints
Blueprints should be named in the Content Drawer using a `BP_` prefix.

## Editing a Blueprint
To open the Blueprint Editor, you can edit a Blueprint Class by either:
1. Clicking on the Blueprints icon in the toolbar and selecting Open Blueprint Class.
2. Double clicking on the Blueprint Class in the Content Drawer.
3. Selecting a BluePrint Class from the Outliner and clicking Edit in Blueprint from its Details.

## Blueprint Editor
The Blueprint Editor is used to edit the properties and logic for your Blueprint Classes, as well as their visual appearance.

#### Viewport
The Viewport shows the visual representation of a Blueprint and its Components. It has similar controls to manipulate Components as the Level Editor.

#### Construction Script
This is a special function that all Actor Blueprints perform when the Blueprint is first added to the Level or when an instance is spawned at runtime.

#### Event Graph
The Event Graph is used to program the behavior of a Blueprint.

An Event Graph consists of `Events` and `Actions` that are displayed as nodes which are connected by wires.

You can move around the Event Graph by right-click and dragging and zoom in and out with the middle mouse wheel.

#### Components
Components are ready-to-use objects such as Static Meshes, lights, sounds, colliders, particle systems, and cameras that can be added to Blueprints. To do this, click on the Add button of the Components panel.

The properties of a selected Component can be edited on the Details panel and their visual representation can be edited in the Viewport.

#### My Blueprint
This is a panel where we can create things like Variables, Macros, Functions, and Graphs for the Blueprint.

New things can be added by clicking on the Add button or the + button next to each type. Properties can be edited in the Details panel.

#### Variables
Variables are properties that hold a value or reference an Object or Actor in a level. Variables are typically used to hold things for later use.

Variables can be created the + button in the Variables category in My Blueprint.

Each variable has a specific type of data it can hold. The full list of variable types in Unreal Engine can be found  [here](https://docs.unrealengine.com/5.4/en-US/ProgrammingAndScripting/Blueprints/UserGuide/Variables/).


## Programming with the Event Graph

#### Nodes
Blueprints consists of nodes connected by wires. Nodes are created by right-clicking on an empty space. Each node has a collection of pins which serve as inputs or outputs for the node.

#### Wires
Wires connecting nodes are created by dragging from an output pin and releasing on an input pin. These create one of two paths between nodes, execution paths and data paths.

#### Execution & Data paths
The white pins are called execution (exec) pins. The other pins are the data pins. 

The execution of the nodes in a Blueprint starts with an event node, and then follows the white wire until it reaches the last node.


### Events
Unreal Engine uses Events to inform the state of a game for an Actor. This includes events like:
- Collision Events
- Input Events
- Events signalling the Beginning or Ending of runtime
- Event Ticks which are called each frame
- Custom Events created by the developer

Events are displayed as red nodes in the Event Graph. 

Here is the full list of Events in Unreal Engine ([link](https://docs.unrealengine.com/5.4/en-US/events-in-unreal-engine/)).

#### Custom Events
Custom Events provide you with a way to create your own events that can be called at any point in your Blueprint's sequence

Documentation [here](https://docs.unrealengine.com/5.4/en-US/custom-events-in-unreal-engine/)


### Comments
Comments can be used to describe collections of nodes. Creating a comment also allows all of the enclosed nodes to be moved as a group. To create a comment, select multiple nodes by dragging a box around them and pressing C.

Here is the documentation ([link](https://docs.unrealengine.com/5.4/en-US/comments-in-unreal-engine/)).


### Setting variables and logging output

Important Nodes:
- [Event BeginPlay](https://docs.unrealengine.com/5.4/en-US/BlueprintAPI/AddEvent/EventBeginPlay/)
- [Print String](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Development/PrintString?application_version=5.4)

### Object Interaction

Important nodes:
- [Branch](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/Utilities/FlowControl/Branch)
- Add operator
- == operator
- Cast To


### Destroying and Spawning Actors

Important Nodes:
- [Destroy Actor](https://dev.epicgames.com/documentation/en-us/unreal-engine/BlueprintAPI/EditorScripting/LevelUtility/DestroyActor?application_version=5.4)
- [Spawn Actor from Class](https://dev.epicgames.com/documentation/en-us/unreal-engine/spawning-and-destroying-unreal-engine-actors)
