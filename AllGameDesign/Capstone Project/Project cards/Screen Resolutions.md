---
Sprint:
  - Sprint4
CurrentTask: false
Type:
Due Date:
Is Done?: true
Description: Add more resolutions support
---
Next week, talk about a handoff would look like
it really were client a handoff would be needed, documentation, next steps, training doesn't make sense. 
Final Demo and final presentation will be it
Been spot on, easy and fun. Awesome to work with you

IT WAS ALL WRONG
my viewport size was too large, needed to decrease the size so that things can be properly sized for the game. 
I also had the screen on integer Stretch scale mode instead of fractional which changes how the game window clips content, when in integer mode it cuts content and when it is smaller than the viewport size. By changing to fractional it allowed things to be shrunk. By shrinking the viewport of the project integer mode works but several things break with my UI as it wasn't meant for the small pixels. 

Not 100% sure what next steps are, but swapping to a small dispaly size for base may be best 

Ok, so when changing resolutions the size of the canvas needs to be adjusted to fit these new sizes. Dynamically doing so will require a bit of code and setting up getters and setters. More importantly it will also require making sure nothing looks bad in those resolutions

I would like to have it at least be set up to get and set the resolution even if it can only do 1 type (1920 by 1080)

1024by768
1152by864
1176by664
1280by720
1280by800
1280by960
1280by1024
1360by768
1366by768
1600by900
1680by1050
1768by992
1920by1080
2560by1080
2560by1440
2560by1600
