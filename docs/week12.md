## Unreal_Engine_Workshop  

### W E L C O M E ! !

Today, we’ll meet as a group to discuss:

- Replacing the Default Animation Blueprint  
- Creating and Using a Blend Space for Movement  
- Adding a Jump State and In-Air Detection  
- Implementing a Run Input Action  
- Editing Animation Sequences in Level Sequencer  
- Connecting Variables Between the Character Blueprint and the Animation Blueprint  


### Custom Animation Blueprint Setup in UE5.6  
This week, we’ll replace the default Animation Blueprint used by the Third Person Template with a new, simplified version.  
The new blueprint will include a Blend Space for idle, walk, and run transitions, a jump animation, and a Run input action to control movement speed.  
You can use the SK_Mannequin or your own custom character mesh as the target skeletal mesh.

You’ll learn to:  
- Create a Blend Space for movement  
- Replace and configure an Animation Blueprint  
- Add transitions for jump and falling states  
- Use an input action to control running speed  
- Edit and segment animation clips in Level Sequencer  

### Creating a Blend Space for Movement  
Steps:  
1. In the Content Browser, right-click → Animation → Blend Space.  
2. Choose your target Skeletal Mesh.  
3. Name it BS_IdleWalkRun.  
4. Open the Blend Space and set the first horizontal axis. Rename it Horizontal and set the Range to 0–600.  
5. Place Idle animation at 0, Walk at around 200, and Run at 600.  
6. Shift-dragging locks clips to percentage increments along the blend axis, helping keep spacing even.  
7. Ctrl-dragging moves the X icon and previews the blend at that specific state, allowing you to fine-tune transitions.  
8. If the blend feels too abrupt, adjust the Weight value (for example, set it to around 5) to smooth out transitions.  
9. Preview with the Horizontal slider to confirm smooth blending.  
10. Save and close.

### Building the New Animation Blueprint  
Steps:  
1. Right-click in the Content Browser → Animation → Animation Blueprint.  
2. Choose your target Skeletal Mesh.  
3. Name it ABP_NameOfYourSkeletalMesh.  
4. Open the blueprint and create variables:  
   - Speed (float)  
   - IsFalling (boolean)  
5. In the Event Graph:  
   - Use Try Get Pawn Owner → Cast to ThirdPersonCharacter.  
   - Use Get Velocity → Vector Length → Set Speed.  
   - Use Get Character Movement → Is Falling → Set IsFalling.  

### Setting Up the State Machine  
1. In the Anim Graph, add a State Machine node named Locomotion.  
2. Inside the State Machine, create two states:  
   - IdleWalkRun  
   - Jump  
3. In the IdleWalkRun state:  
   - Add a Blend Space Player node using BS_IdleWalkRun.  
   - Connect the Speed variable to the Blend Space input.  
4. Add transition rules:  
   - From IdleWalkRun to Jump → IsFalling is true.  
   - From Jump to IdleWalkRun → IsFalling is false.  
5. Assign appropriate animations for each state (for example, Jump_Start, Jump_Loop, Jump_End).  

Note: In Unreal Engine 5.6, state transitions support automatic rule-based transitions.  
If you leave a transition without a defined rule, the engine can automatically evaluate timing and blend weights to create a smooth transition between states.  
This can be useful for testing, but explicit rules are recommended for consistent results.

### Replacing the Template’s Animation Blueprint  
1. Open the ThirdPersonCharacter Blueprint.  
2. Select the Mesh component for your Skeletal Mesh.  
3. In the Details panel under Animation → Anim Class, assign ABP_NameOfYourSkeletalMesh.  
4. Compile and save.  
Your new Animation Blueprint now controls the character’s locomotion and transitions.

### Adding a Run Input Action  
We’ll use the Input Action system to create a Run toggle that adjusts the character’s movement speed.  

Steps:  
1. Open Edit → Project Settings → Input → Actions.  
2. Add a new Action Mapping named Run.  
3. Assign a key (for example, Left Shift).  
4. In the ThirdPersonCharacter Blueprint, create a new boolean variable named IsRunning.  
5. Create an InputAction Run event.  
6. On pressed: set IsRunning = true.  
7. On released: set IsRunning = false.  
8. In the Event Graph (Tick or Movement section), use a Branch to check if IsRunning is true.  
   - If true, use Set Max Walk Speed (on the Character Movement component) to increase speed (for example, 600).  
   - If false, use Set Max Walk Speed to return to the default value (for example, 300).  
9. Compile and test in Play mode.  
Holding the run key should now increase the character’s movement speed dynamically, and the Blend Space will automatically blend between walk and run animations.

### Editing Animation Sequences in Level Sequencer  
Level Sequencer can be used to edit or segment imported Animation Sequences.  
This is useful when you want to split a single animation (for example, a full jump cycle) into separate clips like Jump Start, Falling, and Landing.  

Steps:  
1. In the Content Browser, right-click an existing Animation Sequence → Create Level Sequence.  
2. Open the Level Sequence.  
3. Add your Skeletal Mesh Actor and the Animation Track for your sequence.  
4. Scrub through and identify where each motion phase begins and ends.  
5. Right-click on the track to trim or split the animation into segments.  
6. Export each segment as a new Animation Sequence (right-click → Bake Animation Sequence).  
7. Reimport the new clips and use them in your State Machine transitions.  
For example, you can create transitions between Jump_Start → Falling_Loop → Landing using IsFalling and velocity checks.


### Week 12 Homework: Custom Animation Blueprint Study (Due 11/17)  
Create a short interactive demo showing your custom Animation Blueprint in action. This does not need to be a completed experience. Focus on understanding how the Animation Blueprint and Character Blueprint communicate through input and state transitions.

Your project should demonstrate:  
- A Blend Space controlling idle, walk, and run.  
- Jump logic that includes at least one segmented animation (for example, separate jump and landing).  
- A working input action that drives animation blending or triggers a state in your ABP.  

Estimated Completion Time: ~4 hours.  

### Deliverables  
Create a folder in your class drive named:  `YourName_GMD265_12`
Include:  
- Unreal Project folder.  
- Screenshots: at least 3 images showing your Blend Space, State Machine, and Character Blueprint setup. 
- If you downloaded assets from elsewhere (for example, Mixamo), please be sure to include a `credits.txt` file somewhere in your project. 
