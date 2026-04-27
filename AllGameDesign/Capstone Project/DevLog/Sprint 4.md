
Rex
Hey Rex,

While things may be taking longer to figure out you pointed out the most import part of the process, the lessons you are learning are invaluable. You are finding pitfalls that you will avoid in the future, your understanding of the system you are interacting with are getting more and more familiar. Even if the final project isn't exactly what you hoped for it will be perfect if you can illustrate what it has taught you. 
Enemies are a good choice, and I think it is a decent idea to work on once the desync of NPC's get figured out. One thing I noticed in your code was that the console what showing CharacterBody3D@2, CharacterBody3D@3 ,CharacterBody3D@4,CharacterBody3D@5 bodies that body 5 only displays 2 times while the rest all come in groups of 3. I imagine this is due to the desync issue, but I also noticed the debugger goes up by 2 when you spawn in the 5 npc and house and npc 2 and house. I am pretty sure you already checked but maybe check the spawning code per instance to make sure it is checking the same building list. I know you have the debugger running and having all the NPC printing if they reached target or building, but is there a way to include the instance number (like host, player 1, player 2) so you can see if the error is happening where you think it is it. Alot of the more annoying bugs I had to deal with came from unexpected places.
Thanks for reading,
Harrison

Cody,
This progress is awesome, you have gotten so much done and that is great. I absolutely think a final build with win condition will get done soon. Also I would recommend getting a good start on the UI for the game sooner rather than later, Godot UI is not very intuitive and has a bit of a learning curve that took me a minute to get over. Sometimes it still breaks on me with the smallest changes too. 
Thanks for reading,
Harrison

Retrospective: 
I am working hard on implementing the feedback I received from the playtest, and taking the time to make sure things are working right. For the most important thing I have learned it would have to be screen resolutions and scaling of games, and how your art assets dictate the native resolution you design for. It will continue to use this not only in the upcoming sprint for level design but also for future game projects I will work on. So I don't need much assistance, the weekly check ins are more than enough for me. But my next steps will be working on the level design, getting the various components of the games working together, and finally publishing the demo on itch.io. 

For the new bits I plan to record my final presentation and give a demo of it during the recording, and I would like to get it all wrapped up by the 6-7th of May but the 8th at the latest. I also plan to release the demo on itch.io, so anyone who wants to can visit the page and play the demo for themselves. I also will open my github with my notes of the project and the code used for the project, that way you can see all the progress from first commit to the last. 
## Instructions

Write a one-paragraph retrospective addressing the following:

- What are you doing well that you will continue to do in the next sprint? 
- What is the most important thing that you learned in this sprint? How will you use that lesson in the upcoming sprint?
- What assistance do you need, if any, to be successful in the next sprint? (Even if you don’t need assistance, make sure to describe the next steps in your project and who will complete them.)

new **Write an additional paragraph that describes the following**: 

- When you will give your final presentation
- If you will record your presentation or give it live (your choice)
- If the presentation is live, who will attend and what technology you will use (e.g., Zoom or Teams)