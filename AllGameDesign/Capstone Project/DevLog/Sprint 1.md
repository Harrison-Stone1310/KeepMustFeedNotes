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