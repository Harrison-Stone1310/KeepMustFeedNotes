---
Sprint:
  - Sprint2
Is Done?: false
Type:
  - Coregameplay
Due Date:
Description: Making it so certain objects like curroption spots and blocked walls are removed permenatly while minerals come back each run
CurrentTask: false
---
Ok, so a thought has occured to me
Currently saving minerals mined, curroption, and player inventory to file
Only need Curroption and player info, rest can be forgot on new runs

OK, I think I have it
I will have a restart run func happen in SaveObject instead and all the information from the base data will be start in a dictionary in SaveObject. When a run restarts it just overWrites all the information from the game with the dictionary in saveObject
Then when a room gets entered and goes to reload rom SaveObject the information will be set back to base

We will need a few things
FIRST all the materials and their information from each room
Second, Names of all the rooms,
Third, any information not needing to be changed when runs restart
Once that is ready will be good to go. 