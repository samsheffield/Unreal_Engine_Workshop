## W E L C O M E ! !

Today, we’ll meet as a group to:

- Review your progress.
- Troubleshoot any issues you may be having.
- Discuss how to package builds for distribution.


## Basics of Unreal Engine 5.7 Packaging Builds

### Important Details!
1. You can only produce Mac or Windows builds for the platform you are developing on. This is different from Unity!
2. Packaging a project can take a long time, especially on first build. **Expect to wait and wait.**
3. Avoid packaging on laptops that already struggle with UE5 performance; the process is **very** CPU- and disk-intensive. We have Macs and a PC on our program floor that can handle UE5 builds more reliably.
4. You will need some additional tools, which require a significant amount of drive space
    - Windows: Visual Studio with the necessary C++ components (install size can be 10–20 GB).
    - macOS: Xcode (install size 15–20+ GB, but it should already be installed!)

5. Before packaging, double-check your Project Settings to ensure a default Game Map is set. This prevents the build from loading into the wrong level.

### The Packaging Process
Unreal's Documentation is [here](https://docs.unrealengine.com/5.4/en-US/packaging-unreal-engine-projects/). This is a commercial game engine, so there are _a lot_ of options.

### PC users: Install Windows SDK
On Windows, you will need to install [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/) to build a game for Windows. Otherwise, there will be a greyed out SDK Error under the packaging option for your platform.

### Mac user?
On a Mac, you've already installed XCode when installing Unreal, so you should be good!

### Basic checklist
- Set a default map (`Project Settings > Maps & Modes > Game Default Map`)
- Optional: Set icon files (Project Settings > Packaging)
- Start packaging (`Toolbar > Platforms > Your Platform`. Set Binary Configuration to `Shipping` and then click `Package Project`)
- Create a new folder called `Builds` and select it for packaging.
- To share your packaged project you will need to provide a player with the _entire packaged folder_, not just the executable file. Note: this looks different on Windows and Mac. 

#### Changing the Packaged Project's Name
Unfortunately, this is sort of clunky...

1. Close the Unreal Engine (or make sure your project is not open!)
2. Locate the .ueproject file in your project folder (the one with the fancy UE icon)
3. Rename it and then reopen it before packaging it up again.

#### To change what is displayed as the tile
- Under `Project > Description` set the `Displayed Project Name`

#### Create ICO file
You can convert a PNG to an ICO file using an online service such as [this](https://www.icoconverter.com/).

### What now?

#### Test your build
- Navigate to your build folder.
    - On Windows: run the .exe file inside the Windows build folder.
    - On Mac: open the .app bundle.

Confirm that:

1. The correct default map loads.
2. Controls and UI work as expected.
3. Performance isn’t worse than in PIE (Play In Editor).

#### Clean up / iterate

- If something’s broken, fix it in the project and package again.
- Suggestion: Keep old builds in labeled folders (v1, v2, v3) so you can roll back if needed.


## Complete Final Project (Due next week)

The Final Project is due at the start of class next week. A full description can be found on Canvas.

### Next Week's Class
- 9:00: Arrive to class and get set up (**do not attempt to package your project at this time. It will not be enough time!**)
- 9:30-10:30: Check out projects on your computers.
- 10:45 - ??:??: Feedback session (15 minutes each: Tell us about your work, we'll tell you our thoughts!)
- **Don't forget to upload your files to the class Picasso server.**
