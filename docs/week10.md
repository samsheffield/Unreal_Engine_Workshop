# W E L C O M E ! !

Today, we'll meet as a group to discuss:  
- User Interface (UI) Widgets  
- Game Modes and Game Instances  
- Player Controller Input Modes  
- Binding variables from Player Character and Game Mode Blueprints  
- Persistent score systems across levels  

---

## Video Demos

Weekly demo videos can be found on our class Canvas Welcome page. I will have new videos posted no later than Wednesday evening most weeks.

_Need a specific demo?_ Let me know!  

---

## Reminder: Unreal Engine 5.6 Documentation

In addition to what we cover in class each week, the best place to look for additional information is [the official documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation).  

---

## User Interfaces, Game Modes, and Game Instances in UE5
This week, we’ll focus on creating interactive UI systems connected to gameplay logic. We'll explore how Widgets, Game Modes, and Game Instances work together to provide persistent game data, such as a score, and how to manage Player Controller input modes and mouse visibility.  

### Creating UI Widgets

- Introduction to Widget Blueprints  
- Layout basics (Text, Image, Button)  
- Binding a Text element to display a score or other gameplay variable  
- Connecting Widgets to Player Character and Game Mode variables using bindings and casting  
- Adding interactivity with buttons:  
  - Trigger a Custom Event in the Game Mode  
  - Open or load a new level while preserving data  

### Working with Game Modes

- Use Game Mode Blueprints to manage gameplay rules and events  
- Create a `Score` variable and a Custom Event (e.g., `UpdateScore`)  
- Demonstrate updating the Game Mode from UI interaction  
- Show how Game Mode communicates with Game Instances for data persistence  

### Using Game Instances for Persistent Data

- Create a Game Instance Blueprint to store persistent variables like score  
- Access the Game Instance from multiple levels to retain data across level transitions  
- Combine with Game Mode Custom Events to ensure data is saved and updated correctly  

---

### Player Controller Input Modes

- Configure Player Controller for UI interaction:  
  - Set Input Mode UI Only or Game and UI  
  - Enable Show Mouse Cursor = true (check the box)
- Ensure buttons and interactive widgets respond correctly to clicks  

---

### Binding Variables

- Demonstrate binding variables from Player Character Blueprint and Game Mode Blueprint to UI elements  
- Update the UI dynamically based on gameplay events  
- Example: Press a button → triggers Game Mode Custom Event → updates score → UI updates in real time  

---

## Week 10 Homework: UI and Level Progression Study (Due 11/03)

### Assignment Details
Create a small interactive prototype demonstrating:
- Level transitions
- Persistent data using a Game Instance
- UI Widgets connected to gameplay events
- Player Controller input setup for interacting with UI

### Estimated Completion Time: ~5 hours

Focus on making the project interesting and effective at communicating your ideas and reinforcing goals. Do not spend too much time polishing 3D assets this week; focus on the appearance of UI elements. 

**If any part seems to be taking particularly long, reach out to me via email, or visit our TA in the Game Lab on Wednesday afternoon, for guidance.**

---

### Project Structure Requirements

1. Start Level
   - Title
   - Includes a UI Button to begin the game
   - Uses imported font
   - Button triggers opening the Main Level
   - Optional: introductory instructions or description

2. Main Level
   - Player interacts with the environment to meet a simple criteria (collect items, trigger events)
   - UI displays score or progress as text
   - Game Mode updates the score or relevant gameplay variables
   - Variables are sent to the Game Instance for persistence

3. Second Level
   - Loads after the Main Level
   - Retrieves persistent data from the Game Instance (e.g., score, collected items, completed objectives)
   - Player can continue interacting with the level to update the score
   - Optional: trigger an End Level once a second-level criterion is met

4. End Level (Optional)
   - Triggered when the second-level criteria are completed
   - Display final score or summary using UI Widgets
   - Can include a simple animation, feedback, or “Game Complete” message


### Deliverables

Create a folder in your class drive named:  `YourName_GMD265_10`

Include:
- Unreal Project Folder: complete project with Start Level, Main Level, Second Level, optional End Level
- Screenshots: at least 3 images showing your game levels
