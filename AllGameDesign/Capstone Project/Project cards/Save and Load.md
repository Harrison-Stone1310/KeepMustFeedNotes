---
Type:
  - Coregameplay
Sprint:
  - Sprint1
Due Date:
Is Done?: false
Description: Save and load the game information, such as player position and minerals acquired.
CurrentTask: false
---
#capstoneProject 
Notes so far:
- Been looking into save an load some more and see the two paths to take are saving with resources and saving with JSON. Already tried with resources so I think it would be best to try with JSON next. JSON is also safer.
- A list of all the info I need saved would a good start, need to decide who handles want. I saw one implementation using a save function in each object that needs to be saved, and adding it to a group called persistent. 
- Because roguelite may need to have a "new run" save function, that only overwrites some of the things but others are kept. 
- Ok, been playing around with JSON save and noticed that Space is auto enabled to hit buttons which may have been affecting my save/load in the keep must Feed first draft. However I have a rudimentary save/load. The issue is they everything I want to add to the save needs to be manual entered into their save function, same with load. 
- Noticed that when tying the save/load code to the player aspect the signals for save load should not be tied to the player code as it needs to be moved into different scenes and breaks. Save load on player should a a function that is called upon that gathers all the information and send it over however that means everything that I want to save will need to do the same, so like if I wanted to save all the enemies info of dead or not they would need to 
- Able to save dictionaries in dictionaries so can make a dictionary of what needs to be saved and send it around via function calls. 
- [[SaveLoad UML.canvas|SaveLoad UML]]
- One thing is if there should be a dictionary of levels in the save load or if the level itself should be the only one who knows where the connections should be. On one hand having a complete list of all levels and what resources they will be using is a good idea and on the other the level idenpendatly storeing the data...actually that would be bad because it would lead to alot of repeat saved data that isn't necessary. Just know the level number and nothing else should be enough, then a master dictionary list that allows for things to get updated in Save Load would work best.
- There should be a secondary save file that isn't altered called BaseLoad and it should hold all the information necessary for clearing the board for runs
- Ok, so there is a concept that I am looking into for the scene transition that involves have a level controller and keeping scenes in memory and only deleteing when not in use. This concept is high level and would work really well for my game (like a state machine but for scene transitions. )
- If levels are going to be self contained than for saving and loading going to need to have getters and setters for any parts saved, could do it where you send 2 parts to the function 1 is the Data and the other is the identifier
- 11/2 NEED a way to parse through the game save information when it is saved, also important that when the game is saved and loaded **Everything** that needs to be saved is saved as the save code overwrites the file, it does not add onto it. 
- 11/9 Using int as keys results in the keys becoming strings when saving and loading, probably best to give all the rooms String keys instead. *OK* so I think making it so when something that needs to be saved gets changed then that is when Save(object type) gets called.
