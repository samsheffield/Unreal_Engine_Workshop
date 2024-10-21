# Open Exploration Project 1 Reviews

## Project Presentations & Reviews
We'll dedicate most of today's class time to reviewing your projects _starting at 5pm_. If you would like additional 1-on-1 feedback on your work, please schedule an appointment with me during open office hours.

### Format
- Each person/team gets up to 15 minutes to present and receive feedback.
- Demo your project using your laptop (preferable) or the classroom projector. 
- Have a volunteer ready if you want someone else to play your project.
- Tell us what your goals were for the project.
- Give general feedback as an audience. If you'd like feedback on something specific, please let us know.


### Don't forget to turn in your work!
In the `lastname_firstname_project1` folder you created for homework two weeks ago, add the following:

- 3 high quality screenshots from UE5 which shows different views of your completed project. _Don't forget to toggle Game View to remove the XYZ orientation widget._
- Completed Unreal Engine Project. _Make sure to upload the project folder and all of its contents!_


# Homework

## UMG GUI Demo
This weekend, you'll be getting a headstart on our next topic of discussion- creating User Interfaces (UI). [Here is a video](https://youtu.be/bULo0uMeqWM?si=ras4GC2x30rzBqsO) demo which I've created to demonstrate the basics of UI creation in UE5.

## For next week
Follow along with my demo and create a new UE project which includes:
- A custom Game Mode Blueprint
    - Set this as the Default Game Mode in `Project Settings > Maps & Modes`.
    - This needs to be set up to use the BP_ThirdPersonCharacter as Default Pawn.
- A Widget Blueprint for UI
    - This should be set up to display an item count which we will update through interaction next week.
    - Include the following widgets: Canvas, Text
    - Don't forget to anchor the UI widgets
    - Import and use a custom font for the UI Text
- Blueprints for a "collectable" item
    - For now, the Blueprint's Actor should be destroyed using OnBeginOverlap
    - Next week, we'll keep count and reflect this in the UI

__Bring this in-progress UE project to class next week as a jumping off point for further discussion on how to update the UI in realtime.__