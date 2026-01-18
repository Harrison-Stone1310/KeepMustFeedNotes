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
11/23: What if instead of bring the player to the scene, brought the scene to the player? NOTE: This does work, a manager that has the scene paths can in fact handle the transitions. Could have it where when the level calls the scene transition code when hitting the level borders. Left for later

12/20: Watched a video on the idea that defining the idea the having the doors between levels defined twice is a bad design choice. Example is When making cutting room 1 transition to cutting room 2 both scene have defined in their code where they transition to, and if I made the mistake of setting up the code wrong then 1 could go back to 1 or to 3 even though it is meant to connect to two. Single Source of Truth is the conecpt

After testing here are the summary notes on what a scene needs for transition
- 1 load scene per entrance/exit -see source 1
- 1 signal per load zone that detects when a body that is a player (using player class) enters the zone- see source 1
- a room number/ identifier- see source 1.1, 1.2
- the identifiers of the rooms that it connects to and the side it enders from- see source 1.1, 1.2
- the spawn points of all the entrances (ie if the player enters on the right need to know the x and y of that spot and have it referenceable)- see source 1.1, 1.2
- on ready a check to see where the player will spawn in, and make the player's position be that. - see source 1.1, 1.2
- Then need a global script with the level paths assigned with their - see source 1.4
- ~~New Resource setup; testLevelResource.gd~~ Gonna axe the resource route here, see 1.2 for other version. After all each level is going to need their own script to handle the collistion effects...UNLESS I add that to the resource too. Unceratin, gonna leave it for now
Sources
1) SaveLoadTest project
	1) test_load.gd
	2) test_save.gd
	3) test_player.gd
	4) SaveLoad.gd
Notes
- https://docs.godotengine.org/en/latest/tutorials/scripting/change_scenes_manually.html some guidance on getting scene transitions inorder
- - 11/2 Ok, so on scene transition alot of data is lost but a resource's data is transfered. So I can use a resource to keep the data in use, but on load the resources information is lost. SOOOO I think I can use Save/Load JSON with resources combine to make a functional system of saving and loading data. Using resources to contain the data while running and using Save/Load to contain it between booting the game. 
- 11/9 Doing some scene transition work, trying to get it so that instead of the game sending signals to player who loads based on those signals I am sending a signal via player that then tells the level to transition (I think this is better, need to test it)
- 11/11, Test save Left spawn X:-410 Y:288, Right Spawn X 226 Y 179. Test Load Spawn left X: -343 Y: 33, Spawn Right X: 170 Y: 67. 
	- Okay, able to physically set the spawn points to be used and able to add side enter to SaveLoad global to access the information. Possible to create a full global script library to use instead of SaveLoad, but at this moment it works good to set area entered. However that is being set by the signal of entering load zones in the player's code. Maybe have the load zones instead detect a signal sent by the player? 
- 11/13 Setting up the Player node with a class Name player and have thing level's code have the detection I can set up a simple if statement like below
	- `func _on_scene_load_right_body_entered(body):`
			`if body is TestPlayer:`
				`print("Entered save right new")`
				`SaveLoad.setSideEnter(-1,"Right")`
				`get_tree().change_scene_to_file.call_deferred(SaveLoad.getLevel(-1))`
