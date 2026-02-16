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