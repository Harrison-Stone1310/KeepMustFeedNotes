---
Sprint:
  - Sprint3
  - Sprint4
  - Sprint5
CurrentTask: true
Type:
Due Date:
Is Done?:
Description: Stories from the project
---
I want to start writing up the stories and experiences I have had during this project, condense them all in one spot. Lessons I have learned, decisions I have made, and how I overcame obstacles I faced. That way I can have a place to review those stories for future reference

Refactoring is project management
	One of the things I did during development was refactor my code several times, with two of the biggest times being designing my Room's code and State Machine code. With the State Machine I refactored to use abstract classes for the code to allow for the state machine to be resusable by other entities than the player without copying code. The Room's code was very similar in that when I was beginning to go from the Cutting Rooms to the Main tutorial room I realized I would need to copy about 60% of my code each time I needed to make a new room, and I disliked that. So instead I looked by my abstract level class and began 