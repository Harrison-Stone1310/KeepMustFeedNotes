
Signal Save/Load  
	So advanced signals can send full dictionaries, and maybe even functions to call so with that in mind having it were instead of everything calling a middleman like Level it all instead calls the big guy, saveobject. Saveobject has it sorted by level (each thing saved has their level, and then their other data). This way there is only 1 place things get stored inbetween scene transitions and during gameplay. 
	SEE Future Use TODO to see how to to connect SaveObject signals to ingame nodes


Adding Items to Inventory
	Right now the way items are added is a convoluted system of changes and calls, currently the player mines the materials and once mined material calls minMaterial in Level, which sets the material to be mined and calls a function in the player called add item. For now going to do a minor change and have Gem call add item on pickUp 

Singleton Mineral/Corruption Spot
	So the level resource already holds the below information, would be better to instead have level resource act as the keeper and the various objects go to it based on their names. 
	Making a resource for materials that hold information like Name, Type, Animation Names, and minerals needed that can swap out and change the type to like Topaz or Saphire based on a resource. Default values will be required. 
	On another note, having it so that each thing in the level checks if they already exist in the information and if they don't they add themselves to it. That way setup is a bit easier on the levels (like with minerals, have it call a thing to check if it has been added to level and if not add its information)

Enum Mineral,
	Ok so adding a Enum of types is really easiy and can make it a drop down menu...need to refactor to make that a thing. 

Room Manager
	Make it so all room connections are store in one place, so that rooms will all be correct because their is only one spot