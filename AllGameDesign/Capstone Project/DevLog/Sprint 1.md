Scrum 1 
things done
Implemented a material object, code still a bit jank but it is working. Includes a hit detection animation
Implementing adding and subtraction of inventory to player code, 
Implementing save calls between levels, currently working by calling Save on level and player when exiting scenes and load when readying scenes 
adding to player code
saving between levels
hit detections animations on mineral 
Gosh dangit, found out next level signal logic so can connect things easier than even before and send things easier too. 
Scrum 2
	2/4
	Finished making the minerals and inventory work together, 
	Created initial code for the corruption spots. It is working now and able to take from inventory (only when the amount needed is more than the amount required). Saves with the level loading and make it so that deletes itself when it is out of materials needed
	Added new inventory loaded signal that send a dictionary so that functions can use the dictionary instead of function calls
	Need to make it so that the curruption spot disappearing opens up spaces (Either a door block with opening animation or something else)
	Possibly need to add a loadable script that adds or removes scene children based on their status
	Corruption spots work, disappears on load, works with all 4 minerals, and is good for future work as well. 
	Still need to add a way for spots to open up, probably going to need a door object that is tied to a corruption object
	2/6
		Found a bug with corruption spot, levelData overwriting the corruption spot data when leaving and entering a level without interacting with it first. Fixed by adding correct information to levelData. Was worried about this, idea to implement a singleton structure in the future was already added to Future development ideas and will continue to double check for these bugs when making the demo. 
		Bug: The loading zones exported sides cannot have spaces in them, as they will mess with the logic of loading. Had that issue with CuttingRoom1 loading zone Right have a space after the Left string which broke the code. If delaut is being used but check is correct, check for spaces
	2/7
		Tried to make a resource based level system and After getting the resource to work it became a bit of a problem as SaveObject and the resource and the resource's dictionary conflictied with eachother so it cause the same about. If I am going to do this I think the best way would be to have it use resource's in SaveObject instead of level. Or have it so the resource doesn't us a dictionary at all. Both would be good ideas
		Ok, so the level resource path is working Right now. Making a much more singleton. Works with keeps heart with minimal additional code writing. Going to merge it with main branch and continue making the Keep's Heart Scene
	2/9
		Refactored room code so that Level adbstract class has 90% of the code and rooms have the other 10, now setting up a room takes a few inputs and editing the Room manager
		Keeps heart and Room 1_1 have been made, came up with room naming convention of the 4 corners each have a header (1-4, starting top right and clockwise going up) then each room has a number. This way there can be any number of rooms. 
		Have connected Keeps heart to Room1_1 but not vice versus. 

Retrospective
- What are you doing well that you will continue to do in the next sprint? 
	- I am budgeting time allowances for items with a good amount of learning curve time for items as this is the first time I have done a lot of these aspects with Godot and the added time has allowed me to fully flesh things out
	- I am recognizing where things need to be improved immediately and where things can be put off til later development. I have already refactored several systems like Level/Room code, or the entire game and added a lot to future development ideas. 
	- I am handling project management very well, need little to no guidance with that aspect. Been insuring to make when things are complete and when I am doing things, budgeting time, and ensure to keep myself accountable for how the project is going
	- Been taking what I have learned earlier in the Sprint and applying that to future development, such as making Minerals in my game easily swappable via 2 String names. Would like to make it a drop down in the future if possible. 
- What is the most important thing that you learned in this sprint? How will you use that lesson in the upcoming sprint?
	- There are several key moments of decision making that needed to be made while I was working on Sprint 1, moments of adding things to the Sprint due to the project needing it, choosing to refactor something so future development is easier, and choosing to leave something as it was to development has continue. I viewed these skills as development skills but realize that many of them were project management skills as well, readjusting scope to make next's Sprint easier, choosing to leave something for later so not to exceed time budgets now, and to choose that the time required to refactor now is worth it to make sure next development cycle goes smoothly. I have learned to view these decision as both developer and project manager, and I will continue to do so as I work to get the demo done. 
- What assistance do you need, if any, to be successful in the next sprint? (Even if you don’t need assistance, make sure to describe the next steps in your project and who will complete them.)
	- I don't need any additional assistance, the next steps in the project are to get the demo complete which includes a tutorial and more finished product. I have been thinking of adding a main menu as part of sprint 2 scope but will decide on the necessity of that as Sprint 2 continues.

Feedback
Lost your job (that sucks)
Doing a game (cool)
solitaire with effects
Using Phaser, honestly a good choice. While I never used it before I know it comes highly recommended, when I was at UW Stout there was a class that almost completely used Phaser. 
Simple can be great, there is a reason things like candy crush, flappy bird, and block blast either had or have so much popularity. 

Hey Cody,
First up sorry you had to start over your project due to a new job. That sucks completely. But I will say that I like the way the new project sounds, a lot of people underestimate how good a simple game can be. There is a reason why things like candy crush and block blast got so popular, and solitaire is a great choice. Simple rules, only need one player, and any number of effects work good for it. Using Phaser is also a really good choice, I have never used it before but it came highly recommended when I was at UW Stout in the Game Design program. I still have the page of examples booked marked on my computer. 
Finally for your feed back I don't have anything for learning syntax of JavaScript, nor any libraries to reference. Not only has it been a minute since I coded in pure JS but I never really took got a chance to get to know it well. Generally when I need to find something I turn to W3Schools to start as they have a base of information, but honestly there explanations need a bit of work. 
Thanks for reading, Harrison

Hey Rex,
First up I think that getting the multiplayer functionality up and running first was a good decision, with it being a core aspect of the game insuring that everything works in multiplayer when built is smart. However I am a bit worried about your progress and plan, you say you are behind schedule and you wanted to get building and placement done for in network. However you never showed us your plan for Sprint 2, or talked about what else would need to get shifted due to progress going slower than expected.
My feedback for you would be to take a moment to find out what went wrong with Sprint 1 and why progress was slowed. If it was a one and done issue then maybe some buffer time would be a good investment, I had several major issues happen to me in the last year or so and have added a lot of buffer progress into my project to insure that if something comes up I will still be good to go. If it was more systemic of a problem that will continue through the system than maybe scope of the project needs to be addressed. Last semester I decided to switch from making my project a full game to making a demo due to the size of my scope being too much for me to complete, and it was a fantastic decision that now allows me to take more feedback in and give more polish to what I am making. 
If you have already done this then you beat me to suggesting this and I am so happy to hear it. I love your idea and want to see you succeed, and so I hope you take the time to see what is causing you issue and resolve it so you can succeed and make an amazing game. 
Thanks for reading, Harrison


(Images have numbers, see corresponding image based on number)
First up I have finalized what is needed to be done in Sprint 2 and added those cards into the project (1).  One of the things I noticed I will need alot of is new UI based things, like the Curroption showing what minerals are needed and Tutorial Elements. These are things that I don't have much experience with really and know may take a bit longer or I may find a way for it to be improved when I do it, so I broke some of them down into multiple parts to make sure time is properly budgeted.  

Here is what was completed in the last week for the project
Refactored the room code the Level abstract class have about 90% of the code and each level needs only a few key details to function. This wasn't something that I had a created a card for in the sprint but has made setting up level go 10 times faster. Keep's Heart room and Room1_1 have both been created and tied to each other so the player can move between them freely,(2,6)  remade the levels with new textures, added parallax effects to each level, added first iteration of Keep's Heart asset, added gem pop out and pick up effect for minerals(3), made it so doors opened when destroying curroption(4,5).

Images 
1. ![[Sprint2Overview.png]]
2. ![[KeepHeartPreview.png]]
3. ![[MineralGemPopOut.png]]
4. ![[CurroptionBeforeOpen.png]]
5. ![[CurroptionAfterOpen.png]]
6. ![[Room1_1Overview.png]]
7. 