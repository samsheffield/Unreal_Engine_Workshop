# Work Session
## Open Exploration Project 2 (Due NEXT WEEK, 12/09)
_This is the final open-ended and self-directed in this course. Make something great!_

## Description
Work with the skills you've been developing this semester to make something small with UE5, inspired by your own interests as artists and designers. You are welcome to revisit any of the projects or homework assignments as a starting point for this assignment. You are also welcome to create a small study on some topic that we have not covered in class. However, please do not use the outcome of an online tutorial as your project.

Full description of project is [here](project2.md).

## Weekend Demo: Packaging your projects for distribution

Unreal's Documentation is [here](https://docs.unrealengine.com/5.4/en-US/packaging-unreal-engine-projects/). This is a commercial game engine, so there are _a lot_ of options.


Today I will demonstrate the most basic process of packaging your project so that it's playable on someone else's computer. __I will also have a video of this process for you by Wednesday morning.__

Some important things to note:
1. The first time you package your project, it will take significantly longer than subsequent times.
2. You can only build for limited platform from your computer (For example, Windows PCs can't create MacOS packages and vice versa).

### PC users: Install Windows SDK
On Windows, you will need to install [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/) to build a game for Windows. Otherwise, there will be a greyed out SDK Error under the packaging option for your platform.

On a Mac, you've already installed XCode when installing Unreal, so you should be good!

### Basic checklist
- Set a default map (`Project Settings > Maps & Modes > Game Default Map`)
- Optional: Set icon files (Project Settings > Packaging)
- Start packaging (`Toolbar > Platforms > Your Platform`. Set Binary Configuration to `Shipping` and then click `Package Project`)
- Create a new folder called `Builds` and select it for packaging.
- To share your packaged project you will need to provide a player with the _entire packaged folder_, not just the executable file. Note: this looks different on Windows and Mac. 

#### Changing the Packaged Project's Name
Unortunately, this is sort of clunky...

1. Close the Unreal Engine (or make sure your project is not open!)
2. Locate the Unreal Project file in your project folder (the one with the fancy icon)
3. Rename it and then reopen it before packaging it up again.

#### Create ICO file
You can convert a PNG to an ICO file using an online service such as [this](https://icoconvert.com/). __Beware: This website has an  installer that looks like a required Step 3. Skip Step 3!__

Some options for this website:
- ICO for Windows format
- Convert to ICO (Step 5)
- Click the Download your icon(s) link for the ICO file. 

# Homework

## Wrap Up Open Exploration Project 2 (Due Next Week)
The project description can be found [here](project2.md)

### This week:
Find time this week to _nearly_ complete your project. __Things will need to be completely finished by 5pm next week.__

### Important: What to turn in, where, and when
Create a new folder in your class folder on the Picasso drive called `lastname_firstname_finalproject`. 

In this folder, add the following:

- 3 high quality screenshots from UE5 which shows different views of your work in the UE editor. Don't forget to toggle Game View to remove the XYZ orientation widget.
- Any planning documents, sketches, and reference materials used. Please put inside a folder.
- Completed Unreal Engine Project. Make sure to upload the project folder and all of its contents!
- Optional: Packaged executable application
