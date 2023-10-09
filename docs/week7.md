# Intro to Blueprints 2

## External Hard Drive
I have an external hard drive that I'll begin bringing in each week. Please transfer any classwork you have from week to week.

## Blueprints

### Resources:
- Unreal Engine Blueprint documentation can be found [here](https://docs.unrealengine.com/5.2/en-US/blueprints-visual-scripting-in-unreal-engine/).
- Blueprints Visual Scripting for Unreal Engine 5 - Third Edition ([link](https://www.packtpub.com/product/blueprints-visual-scripting-for-unreal-engine-5-third-edition/9781801811583)).

## Blueprint Flow Control
Documentation [here](https://docs.unrealengine.com/5.2/en-US/flow-control-in-unreal-engine/)

### Branch
Documentation [here](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Utilities/FlowControl/Branch/)

Branch is equivalent to if/else conditional statements in other programming languages.

### Gate
Takes in execution signals, and the current state of the gate (open or closed) determines whether those pulses pass out of the Exit output or not.

### MultiGate
One execution signal split into multiple outputs that are triggered sequentially or randomly.

### Switch
A switch node reads in a data input, and based on the value of that input, sends the execution flow out of the matching execution output. There are several types of switches available: Int, String, Name, and Enum.

### Do N
This node can limit the passing of an execution signal to a specified number of times.

### Do Once
This node can limit the passing of an execution signal to just once.


## Keyboard events
Documentation [here](https://docs.unrealengine.com/5.2/en-US/BlueprintAPI/Input/KeyboardEvents/)

Key events can easily be searched for by using `Key NameOfKey`.

### Important: Enable Input
If you want to use input events you need to make sure your Blueprint has input enabled*. `Enable Input` node connected to...
- Event BeginPlay (input execution path pin)
- Get Player Controller (Player Controller input data pin)

*The player controllers from Starter Content and the Level Blueprint are exceptions to this (The former already has it!)


## Examples:
- Interact with a volume and press a key to trigger an event (two ways to structure conditional logic).
- Conditional flow examples using Switch, Branch, DoN, MultiGate


## Work Session

### Review Project Planning and Blockouts
While you're working, I'll take a look at your project planning (moodboards and blockouts).

### Open Exploration Project 1 (Due after Fall Break)
The project description can be found [here](project1.md)


# Homework

## Fall Break
Take a break!

## Continue Open Exploration Project 1
Find time after the break to complete your projects.

### Important: What to turn in, where, and when

For this assignment, you will turn in:
- Completed Unreal project

If you have space in your online Drive, add it to the folder you've created. Otherwise, transfer it to the external hard drive sometime during our next class.


# Upcoming Events

## STEM Festival Opening Event (Oct 12th)
We've also been invited to participate in the opening event for the MD STEM Festival on the evening of October 12th at Howard County Community College. 

They're looking for any interested students who want to demo their games at the event and they will pay for an Uber/Lyft if you don't have your own transportation. [link](https://marylandstemfestival.org/events/maryland-stem-festival-2023-opening-ceremony).

## Workshop: Unity Dialogue System (Oct 18th)
Tony Li from PixelCrushers will be here to demonstrate their excellent dialogue system for Unity. Come join in and learn the basics from 2:15-3:45 on Wednesday, Oct 18th.