---
Sprint: Sprint1
Description: The second scene that gets loaded when the player enters it
Type:
  - Coregameplay
Due Date:
Is Done?: false
CurrentTask: false
---
#capstoneProject 
- https://docs.godotengine.org/en/latest/tutorials/scripting/change_scenes_manually.html some guidance on getting scene transitions inorder
- - 11/2 Ok, so on scene transition alot of data is lost but a resource's data is transfered. So I can use a resource to keep the data in use, but on load the resources information is lost. SOOOO I think I can use Save/Load JSON with resources combine to make a functional system of saving and loading data. Using resources to contain the data while running and using Save/Load to contain it between booting the game. 
- 11/9 Doing some scene transition work, trying to get it so that instead of the game sending signals to player who loads based on those signals I am sending a signal via player that then tells the level to transition (I think this is better, need to test it)
- 11/11, Test save Left spawn X:-410 Y:288, Right Spawn X 226 Y 179. Test Load Spawn left X: -343 Y: 33, Spawn Right X: 170 Y: 67. 
	- Okay, able to physically set the spawn points to be used and able to add side enter to SaveLoad global to access the information. Possible to create a full global script library to use instead of SaveLoad, but at this moment it works good to set area entered. However that is being set by the signal of entering load zones in the player's code. Maybe have the load zones instead detect a signal sent by the player? 