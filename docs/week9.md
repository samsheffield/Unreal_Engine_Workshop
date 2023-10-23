# Open Exploration Project 1 Reviews

## Online Drives
During Fall Break, I downloaded all work uploaded to the Drive folders I provide them. _If you have a backup elsewhere_, you are free to delete them from your Drive folders to reclaim some storage space.

## Project Presentations & Reviews
We'll dedicate most of today's class time to reviewing your projects. If you would like additional 1-on-1 feedback on your work, please schedule an appointment with me during open office hours (most weeks: M & T 3-5, W 3-4).

### Format
- Each person gets up to 15 minutes to present and receive feedback.
- Demo your project using the classroom projector. 
- Have a volunteer ready if you want someone else to play your project.
- Tell us what your goals were for the project.
- Give general feedback as an audience. If you'd like feedback on something specific, please let us know.


### Don't forget to turn in your work!

For this assignment, you will turn in:
- Completed Unreal project
- Packaged build for your hardware platform (Windows or Mac)

_If you have space in your online Drive_, add it to the folder you've created. Otherwise, transfer it (along with the other project files) to the external hard drive sometime during this class session.

## Packaging your projects for distribution

Unreal's Documentation is [here](https://docs.unrealengine.com/5.2/en-US/packaging-unreal-engine-projects/). This is a commercial game engine, so there are _a lot_ of options.


Today I will demonstrate the most basic process of packaging your project so that it's playable on someone else's computer. I'll also upload a video for you to refer to by Wednesday.

Some important things to note:
1. The first time you package your project, it will take a significantly longer time than subsequent times.
2. You can only build for limited platform from your computer (For example, Windows PCs can't create MacOS packages and vice versa).

### PC users: Install Windows 10 SDK
On Windows, you will need to install [Windows 10 SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/) to build a game for Windows. Otherwise, there will be a greyed out SDK Error under the packaging option for your platform.

On a Mac, you've already installed XCode, so you should be good!

### Basic checklist
- Set a default map (`Project Settings > Maps & Modes > Game Default Map`)
- Set a project window title (Project Settings > Project > Description > Displayed > Project Displayed Title)
- Set icon files (Project Settings > Packaging)
- Start packaging (Toolbar > Platforms > Your Platform. Set Binary Configuration to Shipping and then click Package Project)

#### Create ICO file
You can convert a PNG to an ICO file using an online service such as [this](https://icoconvert.com/). __Beware: This website has an  installer that looks like a required Step 3. Skip Step 3!__

Some options for this website:
- ICO for Windows format
- Convert to ICO (Step 5)
- Click the Download your icon(s) link for th eICO file. 

# Homework

## Package your Open Exploration Project
You only need to create a package for your primary computer platform (Windows or MacOS). 

Onc packaged, test the application and then zip the entire build folder (Rename it from Windows or MacOS to _yourname_project1_uew_). Upload this to your online Drive folder or have it ready to transfer to the external drive next week.

### Blueprints Review Exercise
Haven't been using Blueprints in your class work yet? Here's a good opportunity to review some of the things we've covered so far.

Create a level that has this basic level of interactivity:
- 3rd or 1st person character controller
- A BP class that is destroyed when overlapped by the character (Begin Overlap Event).
- A counter that goes up by 1 and is printed to the screen (Print String) each time the BP class is overlapped by the character
- The level is restarted (Open Level) when the counter reaches or exceeds a certain number.
- Pressing the 1 key also restarts the level.

__You do not need to worry about aesthetics for this assignment.__

#### Important: What to turn in, where, and when
You can either upload the work to your class Drive folder (preferred) or transfer it to my external drive next week.

#### Zip your files before uploading
Please zip your Unreal project folder and name it `yourname_week9_uew.zip` before uploading it. Otherwise, the files may become corrupted in the process.