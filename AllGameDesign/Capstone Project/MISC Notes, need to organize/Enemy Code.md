Components 
Health
Movement [[State Machine for Enemies]]
Hit detection -Enemy hit detect exists on 11 and 12 layers 
Attack detection 

NOTES
-I was working with extending the hit box and hurt box code, at first I wasn't certain it was necessary but by extending the code to have enemy specific code I can have it set the hitbox and hurt box values dynamically so it can be set in code and forgotten (if I want to do this that is)
-Resource is a **global** feature, all creatures with that resource share it.
-Bad for keeping track of things like current health but great for keeping things like maxHealth, speed, damage equal through multiple creatures.
-Better to have resource be loaded by multiple nodes than methods to call from one node
-Animation player is able to load animation library as long as the animated sprite 2d has a name that is the same as the saved node

animation player allows for multiple things to happen during the animations, so things like the death animation can play and then the queue_free() function can be called on the parent. 
