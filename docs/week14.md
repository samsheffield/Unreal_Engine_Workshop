# Skeletal Mesh Introduction

## Reminder: External Hard Drive
I have two external hard drives that you can use to submit classwork each week if you are struggling with online storage caps. Please keep things organized.


## Today:
- Work session
- Begin Skeletal Mesh Animation Introduction (1/2)

## Work Session
During the first half of class, you will have time to work on your final project. I will be discussing project plans with each of you and answering any questions you might have.

## Skeletal Animation Introduction (1/2)

### Demo Goals
This week we'll focus on:
- Importing Skeletal Meshes
- Importing Animations
- Creating Animation Blueprints
- Animation State Machines
- Blending transitions
- Triggering animation

### Skeletal Meshes
Skeletal Meshes are animated meshes created using software like Blender or Maya. They consist of deformable meshes which are posed and moved using an internal structure called a skeleton.

The points that create this structure are called bones.

### Importing Skeletal Meshes and Animation
You can add an .fbx skeletal mesh by dragging it into the Content Drawer. You import the skeletal mesh with bones and any animations separately.

You will probably get a number of warnings in your Message Log. This is okay.

This will result in the creation of three Unreal assets:
- Skeletal mesh
- Skeleton
- Physics Asset

### Importing Animations
Drag your animation FBX files into the content drawer. You can use the default settings for importing the FBX skeletal mesh but you will want to select the skeleton asset matching the skeletal mesh you imported previously.

Once imported, you can double click on the Animation assets to preview them or make adjustments in the Animation Editor.

### Setting up a Blueprint
Add a Skeletal Mesh component to your Blueprint. Set the Mesh property to your skeletal mesh. 

To add a simple looping animation, you can set your Anim to play to an imported animation clip and then change the Animation Mode to Use Animation Asset. If you want anything more complex, you will need to create, and then set an Animation Blueprint.

### Creating Animation Blueprints
An Animation Blueprint controls all of the logic related to the sequencing of a Skeletal Mesh Animation. 

You create one by right clicking in the Content Drawer and selecting Animation Blueprint from the Animation category in the pop-up window. Then you will need to specify your target Skeleton. Name these files with an `ABP_` prefix.

#### Animation Blueprints Graphs
Animation Blueprints have 2 graphs:
- AnimGraph: This is used to create flow between the animation sequences
- Event graph: This is used to create the logic

### AnimGraph
- Asset Browser: Used to add animation sequences by dragging sequences to the graph.

#### Output pose node
This is the animation played.

#### Looping Animation Sequences
Select the sequence player and check the Loop Animation box under settings.

#### Useful nodes:
- Event Blueprint Initialize Animation
- Get Owning Actor
- State Machine

# Homework

## Open Exploration Project 2 (Due 12/11)
The project description can be found [here](project2.md)

### Continue working on your projects
Continue to work on your final projects for this class. Focus on developing a functional, blocked out prototype due for in-class review. _Do not become too focused on implementing finalized assets at this point._