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