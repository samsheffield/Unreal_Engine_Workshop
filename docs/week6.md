# Intro to Blueprints

## External Hard Drive
Some students are experiencing some issues with storage on their Google Drives, so starting next week I will have an external hard drive for you to share your weekly prototypes.

If you are experiencing storage issues, you can remove the uploaded files from your Drive and transfer them to the class storage that I provide next week.

Apologies for the inconvenience.


## Resources:
- Unreal Engine Blueprint documentation can be found [here](https://docs.unrealengine.com/5.2/en-US/blueprints-visual-scripting-in-unreal-engine/).
- Blueprints Visual Scripting for Unreal Engine 5 - Third Edition ([link](https://www.packtpub.com/product/blueprints-visual-scripting-for-unreal-engine-5-third-edition/9781801811583)).

## What is a Blueprint?
Blueprint has more than one meaning in Unreal Engine.
1.  It's the name of the visual scripting language used in the Unreal Engine. 
2.  It's a type of complex game object created using the Blueprint language.

There are two main types of Blueprints: 
- Level Blueprint: Each Level has its own Level Blueprint (and only one).
- Blueprint Class.  These are used to create interactive objects which can be reused in any Level.

## Object Oriented Programming (OOP)
Blueprints are based on the principles of object-oriented programming (OOP). One of the goals of OOP is to bring programming concepts closer to the real world.

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

## Editing a Blueprint Class
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
Variables are properties that hold a value or reference an Object or Actor in the world. Variables are typically used to hold a value for later use.

Variables can be created the + button in the Variables category in My Blueprint.

Each variable has a specific type of data it can hold. The full list of variable types in Unreal Engine can be found  [here](https://docs.unrealengine.com/4.26/en-US/ProgrammingAndScripting/Blueprints/UserGuide/Variables/).


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

Here is the full list of Events in Unreal Engine ([link](https://docs.unrealengine.com/5.2/en-US/events-in-unreal-engine/)).

#### Custom Events
Custom Events provide you with a way to create your own events that can be called at any point in your Blueprint's sequence

Documentation [here](https://docs.unrealengine.com/5.2/en-US/custom-events-in-unreal-engine/)


### Actions
Actions are used to define how a Blueprint will react to an Event that is triggered.

Actions are displayed as different colored nodes based on their type.

### Functions & Macros
Functions are node graphs belonging to a particular Blueprint that can be executed, or called, from another graph within the Blueprint. Functions have a single entry point designated by a node with the name of the Function containing a single exec output pin.

Macros are essentially the same as collapsed graphs of nodes and can be used similarly to functions (with some small differences).

We'll talk more about functions in our next Blueprints session.

### Comments
Comments can be used to describe collections of nodes. Creating a comment also allows all of the enclosed nodes to be moved as a group. To create a comment, select multiple nodes by dragging a box around them and pressing C.

Here is the documentation ([link](https://docs.unrealengine.com/5.2/en-US/comments-in-unreal-engine/)).

## Level Blueprints
A Level Blueprint is a specialized type of Blueprint that acts as a level-wide global event graph. Each level in your project has its own Level Blueprint created by default.

Documentation can be found [here](https://docs.unrealengine.com/5.2/en-US/level-blueprint-in-unreal-engine/).


#### Editing Level Blueprints
To open the Level Blueprint Editor, click on the Blueprints icon in the toolbar. Then, select the Open Level Blueprint option from the dropdown menu.

Level Blueprints are simpler than Blueprint classes and the Editor does not include a Constructor Script or Viewport.


## Example Blueprints

### Creating Blueprints with only Components
1. Rotating Actor
2. Projectile Actor

Components:
- [RotatingMovement](https://docs.unrealengine.com/5.2/en-US/movement-components-in-unreal-engine/)
- [ProjectileMovement](https://docs.unrealengine.com/5.2/en-US/movement-components-in-unreal-engine/)

Concepts:
- Navigating the Blueprint Editor
- Adding Components

### Setting variables and logging output

Important Nodes:
- [Event BeginPlay](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/AddEvent/EventBeginPlay/)
- [Print String](https://docs.unrealengine.com/4.27/en-US/BlueprintAPI/Utilities/String/PrintString/)

Concepts:
- Navigating the Level Blueprint Editor
- Creating variables
- Getting and setting variable values
- Instance Editable property
- Converting data types

### Have a player trigger a level change

Important Nodes:
- [Event ActorBeginOverlap](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/AddEvent/Collision/EventActorBeginOverlap/)
- [Open Level (by Object Reference)](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Game/OpenLevel_byObjectReference/)
- Cast to...
- [Delay](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Utilities/FlowControl/Delay/)

Concepts:
- Checking for collision by type
- Creating Custom Events
- Connecting to other Blueprints
- Changing levels

### Object Interaction

Important nodes:
- [Set Actor Hidden in Game](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Rendering/SetActorHiddenInGame/)
- Add operator
- [Play Sound 2D](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Audio/PlaySound2D/)

Concepts:
- Keeping count with variables
- Hiding actors
- Playing sound

### Spawn projectile actor

Important Nodes:
- [Spawn Actor from Class]()
- [Set Timer by Event]()

Concepts:
- Timers
- Spawning Actors
- Constructor Script


## Review Mood Explorations
Let's spend some time taking a look at everyone's weekend explorations.

## Open Exploration Project 1 (Due 10/23)
The project description can be found [here](project1.md)


# Homework

## Continue Open Exploration Project 1
1. Develop a project moodboard (or moodboards) collecting resources and visual inspiration for your level.
2. Create a functional, blockout prototype due for in-class review. _Do not add finalized assets at this point._

#### Moodboard
The moodboard will be used to collect visual references for your project.

Divide your moodboard into sections which define:
- Core references (what is the overall look/feeling you are aiming for)
- Specific references for key architectural features in the environment

Each section should consist of a mixture of key images and a list of text which describes what you are trying to get from your references.

#### Blockout
A blockout or greybox is a rough draft of a level built quickly using simple shapes and without refined art assets to etablish key relationships between the player and the level architecture. Contemporary games are [all designed this way](https://www.google.com/search?sca_esv=569990595&rlz=1C1RXQR_enUS1055US1055&sxsrf=AM9HkKn1NkQumShg71rvPeikO460Wve1Gg:1696242491915&q=last+of+us+blockout&tbm=isch&source=lnms&sa=X&ved=2ahUKEwizwbvZk9eBAxXeKFkFHUHaDdEQ0pQJegQIDRAB&biw=1746&bih=972&dpr=1.1).

Your blockout can consist of geometry brushes or static meshes but it should [prioritize functionality, not the finalized overall look of your level](https://www.google.com/search?q=blocktober&tbm=isch&ved=2ahUKEwj2sZbFlNeBAxUjC2IAHTs_M8UQ2-cCegQIABAA&oq=blocktober&gs_lcp=CgNpbWcQAzIECCMQJzIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABDIHCAAQGBCABFAAWABg2QJoAHAAeACAATaIATaSAQExmAEAqgELZ3dzLXdpei1pbWfAAQE&sclient=img&ei=HZwaZbavMKOWiLMPu_7MqQw&bih=972&biw=1746&rlz=1C1RXQR_enUS1055US1055&hl=en).


### Important: What to turn in, where, and when

For this assignment, you will turn in:
- Exported image of project moodboards
- Unreal project with blockout prototype of your level


I sent out a link to the shared Google Drive folder to your MICA email last week.  __Please have all work uploaded before the start of class next week (10/09).__


# Upcoming Events

## This Saturday: IGDA District Arcade
I was able to secure a table at next Saturday's IGDA District Arcade event in Silver Springs to show off some student games. Let me know if you're interested in participating and have transportation to get there and back. More info [here](https://www.meetup.com/igda-dc/events/295326258/).

_I'll also be there showing an arcade prototype I've been working on!_

## STEM Festival Opening Event (Oct 12th)
We've also been invited to participate in the opening event for the MD STEM Festival on the evening of October 12th at Howard County Community College. 

They're looking for any interested students who want to demo their games at the event and they will pay for an Uber/Lyft if you don't have your own transportation. [link](https://marylandstemfestival.org/events/maryland-stem-festival-2023-opening-ceremony).