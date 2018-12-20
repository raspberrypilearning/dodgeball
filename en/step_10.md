## Challenge: improved gravity

There's one other small bug in your game: gravity doesn't pull the character sprite downwards if __any__ part of the sprite is touching a blue platform. So even if the sprites head touches a platform, the sprite doesn't fall! You can test this yourself: make your character climb most of the way up a ladder, and then move the character sideways beneath a platform:

![screenshot](images/dodge-gravity-bug.png)

To fix the bug, you first need to give your character sprite new trousers that have a different colour (on __all__ costumes).

![screenshot](images/dodge-trousers.png)

Then replace this code block: 

![blocks_1545305688_7672868](images/blocks_1545305688_7672868.png)

with this code block:

![blocks_1545305690_8529701](images/blocks_1545305690_8529701.png)

To make sure you've fixed the bug, test the game after you've made these changes!
