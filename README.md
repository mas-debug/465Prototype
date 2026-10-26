IMS465 Prototype 1.
The mechanic I prototyped from Week 1 is parkour from the Assassin's Creed franchise. I wanted to capture the essence of jumping from object to object with ease depending on where the player camera is looking. The mechanic tells me if an object I raycast to is interactable for parkour or not.

My early and late initialized code is in the PlayerController script. I used awake to initialize the character controller and the main camera object prior to any other code running. I used start for a few other variables that needed to be initialized.
Time.deltaTime was used in the movement method in the PlayerController script to control the speed of the movement.
I made the interface: "IInteractable" to find out if an object is interactable or not for parkour. Inside, I added a method that I used in the ParkourSurface script to run and tell the player what it is interacting with.
I used Unity's Input System to create movement and the character controller. (Note: I originally planned for a third person controller but I could only get the movement to work, then I tried a tutorial and it failed again. I finally swapped to first person in order to complete it.)
I had to shrink and cut from my original idea in week 1 due to knowledge constraints. I planned to make the character jump to boxes in unity, but I cut it down to a player character that works, and being able to raycast to objects to see if they are interactable or not.

DevLog
Date & Milestone Target: What were you working on during this entry?
For this entry, I had 3 weeks to expand on my original mechanic which was a first person character controller and a raycast that would identify if an object had an interface. My goal by the end of this sprint was to have the player teleport to the middle of each box after pressing an interact button, as well as having the player move at a constant speed to each box after pressing the button. 
Features Completed & Progress: What got implemented and merged into the project?
In the time span, I was able to complete both of my original goals. I added to my interface to grab the parkour position of a gameobject, and made a working teleport in the player script for when it interacts. I also implemented a coroutine that would use Lerping to move the player from its original position to the top of each box. I merged it into the project successfully, and made a boolean to turn off actions from the player until the parkour was done. I did not complete any P1 goals before the due date however. 
Engineers' Journal:
What technical hurdles or architectural road blocks did you run into?
How did you solve them?
Did you have to adjust your sprint scope mid-week? Why?
I ran into a few issues during my time working on this project. The first issue I ran into was my entire project overwriting itself. The entire project overwriting itself turned out to be an easy fix, as I could take my code from the github and reuse it in a new project that isn’t messed up. 
Another issue I ran into was my player would sometimes not respond to the interact input and teleport to another cube. I realized that I was incorrectly using bounds for the player, and could use the controller instead to find the bounds and create a proper offset so the player didn’t end up inside of a cube.
When I got to lerping and moving the player from point A to B, I struggled on how to figure out the best way to implement it. I used a video tutorial and scrolled through some code from last year to look for possible solutions. I remembered coroutines after looking at my old code and decided to use one to move the player here. With the help of the video I successfully implemented lerping into my project and made it frame rate independent with Time.deltaTime.
I did not have to adjust my scope mid week, I set it at a good place to achieve it by the due date.
