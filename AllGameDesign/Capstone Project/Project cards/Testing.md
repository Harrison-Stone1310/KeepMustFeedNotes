---
Sprint:
  - Sprint1
CurrentTask: false
Type:
Due Date:
Is Done?: false
Description: Testing
---
Feedback: What is one feature you think would improve this game, either as it is or a future addition
New card for testing notes

GUT needs to have any testing scripts start with test_ and end .gd, which is honestly ok but hate to have that fact not started in the start up guide
All code tests need to be test_ too
For adding a scene to the testing you can use test_SavingLoading.gd as an example, it added the player scene for testing
TODO
- rework player movement state machine to use abstract classes
- [x] test save file system
- [ ] implement new saving and loading of levels
- unit test new saving and loading of levels
- Rework HitBox and HurtBox to use classes and getter logic
NOTE: When saving and loading it will not be the same values between the processes, IE when saving to the file it will not match the values outside of the file perfectly and vice versa. ACTUALLY it is the same, but saving sorts it differently and that makes things the test fail even though it is saved. 