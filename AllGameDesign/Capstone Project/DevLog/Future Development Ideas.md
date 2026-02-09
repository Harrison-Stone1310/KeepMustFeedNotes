
Signal Save/Load  
	So advanced signals can send full dictionaries, and maybe even functions to call so with that in mind having it were instead of everything calling a middleman like Level it all instead calls the big guy, saveobject. Saveobject has it sorted by level (each thing saved has their level, and then their other data). This way there is only 1 place things get stored inbetween scene transitions and during gameplay. 
	SEE Future Use TODO to see how to to connect SaveObject signals to ingame nodes


Singleton Mineral/Corruption Spot
	So the level resource already holds the below information, would be better to instead have level resource act as the keeper and the various objects go to it based on their names. 
	Making a resource for materials that hold information like Name, Type, Animation Names, and minerals needed that can swap out and change the type to like Topaz or Saphire based on a resource. Default values will be required. 

Room Manager
	Make it so all room connections are store in one place, so that rooms will all be correct because their is only one spot