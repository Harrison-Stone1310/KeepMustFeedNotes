---
Sprint:
  - Sprint2
CurrentTask: false
Type:
  - Coregameplay
Due Date:
Is Done?: true
Description: The second scene that gets loaded when the player enters it, second part 2
---
RoomConnects
Room connects have 2 things saved, their parent room and their name
Room manager has the Parent rooms and their connections saved, each connection is unique so only have to list it once. SpawnPoints are based on connections
Instead of this (below)
Keeps Heart to Room1_1_1 Via E1
Room1_1_1 to Room1_1_2 via E2
Room 1_1_1 to Room1_1_4 via E3
Room 1_1_1 to Room
Do this
Room1_1
E1 Connects Keeps Heart to Room1_1_1
E2 Connects Room1_1_1 to Room1_1_2 
E3 Connects Room 1_1_1 to Room1_1_4
E4 Connects Room 1_1_1 to Room1_1_4
E5 Connects Room 1_1_4 to Room1_1_3
E6 Connects Room 1_1_3 to Room1_1_2
E7 Connects Room 1_1_3 to Room1_1_2
E8 Connects Room 1_1_4 to Room1_1_3
E9 Connects Room 1_1_4 to Room1_1_5
E10 Connects Room 1_1_5 to Room1_1_2
E11 Connects Room 1_1_2 to Room1_2_1


Current logic
loading zones emit a player entered signal, which connects to the player ented() in level.gd
The saves the player and calls level Save() too
then using the side entered it gets the Room ID of the new room and calls ChangeScene()
whcih also calls Save() (so a second save)
and Roomanagers, setting side enter, and roomer manager changeSchene 
And that emits a signal to sends the room ID path to Games manager
Which then loads the room into the level. 
Gonna be honest, with new setups can probably bypass all of that in just the loading zone
In loading zone have it
call player save
level save (via get parent)
RoomManager SetSideEnter (will need to edit)
Actully avoid that too, just add Entrance="" to the rooms Dictinonary
Set it in changeScene2
Then have the emit roomChange ne the roomPath gotten in chagneScene2

E6 gap-12 blocks
inbetween 20 blocks
E7 gap-22 blocks

![[Pasted image 20260225185925.png]]