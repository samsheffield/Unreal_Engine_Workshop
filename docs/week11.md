# Creating User Interfaces

## Unreal Motion Graphics (UMG) UI Designer
Unreal's documentation can be found [here](https://docs.unrealengine.com/5.4/en-US/umg-ui-designer-for-unreal-engine/).

The UMG is a visual system for creating user interfaces in the Unreal Editor.

Unreal's documentation can be found [here](https://docs.unrealengine.com/5.4/en-US/umg-ui-designer-for-unreal-engine/).

## Review UI Basics & Game Modes
- Widget Blueprints (Creating, Updating, Adding to Viewport)
- NEW: Setting Game Mode in [World Settings](https://dev.epicgames.com/documentation/en-us/unreal-engine/world-settings-in-unreal-engine)

## Adding and Removing UI Widgets
Here is Unreal's documentation on creating Widgets ([link])(https://dev.epicgames.com/documentation/en-us/unreal-engine/creating-widgets-in-unreal-engine)
Useful Nodes:
- Create Widget
- Add to Viewport
- Remove from Parent

## New UI Widgets
- Image
- UI Panels (Organizing widgets with Vertical Box, Horizontal Box)
- Buttons (& how to use then to trigger actions)

## Adding Player Input Actions
Unreal has a very powerful and flexible system for managing player controls called the Enhanced Input system. Documentation on this system can be found [here](https://dev.epicgames.com/documentation/en-us/unreal-engine/enhanced-input-in-unreal-engine?application_version=5.4).

Two of the most important parts of this system aer Input Actions and Input Mapping Contexts. Today we'll discuss:
- Creating Input Actions
- Adding Input Actions to an Input Mapping Context (IMC_Default)

## Creating World-space UI
Widget Blueprints can be added as components to other Actors or Blueprints.
- How to work with the Widget Component
- Turning off shadows (Requires a Blueprint: Set Cast Shadow) 
- Rotating the Widget component to face the camera (Requires a Blueprint)

## Animating UI
- Open the Animation window in the Widget Blueprint Editor if it is not already open. `Window > Animations`
- Animation is done by manipulating properties of widgets at various keyframes along a timeline. The properties are interpolated between keyframes.

### Playing UI Animation
UI animation will not automatically play. Instead, a Blueprint node is used to start playback. Each Animation is added as a variable to a Widget Blueprint as it is created.

Useful Nodes:
- Play Animation
- Get User Widget Object

## Demo Video:
A video of today's demo can be found [here](https://youtu.be/h94ebz90vyw?si=PH1trg49kmQIWx1S).

# Homework

## Landscape Tools Demo
This weekend, you'll be getting a headstart on our next topic of discussion- working with the Landscape Tools. __I'll add a link to a demo by Wednesday morning__ which I've created which demonstrates the basics of Landscape creation in UE5.

## For next week
Create a small level with the landscape tools that leads a player to a destination using either a first or third person character controller. You will add foliage and a spline-based path to this level next week in class.

Follow along with my demo and create a new UE project which includes:
- Two levels:
    - One level is a Start screen and should include a Widget Blueprint that has text, an image, and a button which loads a game level.
    - One level is a small landscape that has a goal indicated with worldspace UI. Reaching this goal should return to the Start screen.
    - A pause menu with two buttons: RESUME (exits pause mwnu) and RETURN TO TITLE (exits to Start screen).

__Important: You will need to make a Game Mode Blueprint for each level and set them in the World Settings panel. If you only set a Game Mode in Project settings it will appear that the UI from the Start screen is not going away.__ [What's World Settings?](https://dev.epicgames.com/documentation/en-us/unreal-engine/world-settings-in-unreal-engine)

Don't get bogged down in high realism for this assignment. My recommendation is to experiment with the tools and use _reference imagery_ to set some visual goals for yourself. Also, don't forget to use use basic things like light, color, and shape to encourage players towards their destination.

__Bring this in-progress UE project to class next week as a jumping off point for further discussion on working with the Landscape Tools & Foliage Brushes.__

## Upcoming Opportunities

### Career Development's Practice & Pie Event on 11/13
Practice & Pie is for students from all years and majors who would like to build industry relationships and practice talking to people in a professional setting.

For Game Design folks, there will be representatives from Zenimax, Transperfect, and Game4Good in attendance.

Registration for this event is required.  Sign up on the [MICA Network](https://www.mica.edu/career-development/micanetwork/). It often fills up quite quickly, so don't hesitate if you're interested!

### Tronster Hartley (Firaxis) Talk & Pizza next Thursday(11/14)!
Tronster will be visiting us on Thursday, 11/14 to give a talk in D200 at 3pm. There will also be limited 1-on-1 meeting slots prior to his talk available for GMD seniors and juniors (Majors or Minors). Sign up [here](https://docs.google.com/spreadsheets/d/1URrGk762wzcdL3lx74xGpE4OnkWGKfv6uvTlrMrHITs/edit?gid=0#gid=0).

_Tronster Hartley is a seasoned game developer with experience building video games for PCs, mobile devices, Facebook, and major gaming consoles. For the past 16 years, he has been a Senior Software Developer and Team Lead at Firaxis Games in Sparks, MD. He has led UX and UI teams for acclaimed titles such as Civilization VI and XCOM: Enemy Unknown. Currently, he is heading the UX and UI team for Civilization VII._

_In his spare time, Tronster actively promotes the video game industry, especially around Baltimore. He occasionally teaches as an adjunct professor at UMBC or UBalt. As the chair and a founding member of Baltimore's International Game Developers Association (IGDA) chapter, he helps foster the local game development community. He also created the MAGFest Indie Videogame Showcase, featured annually at the MAGFest convention in Washington, DC._

### Narrative Design Visitor This Week!
If you took Narrative Design last year, you're welcome to join this semester's class in a Visual Novel workshop/talk led by [Caroline "Mado" Zeghibe](https://madocactus.itch.io/) this Wednesday from 4-6:30 in D240. _Please let me know in advance if you're interested in participating._