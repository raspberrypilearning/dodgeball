## Gravity and jumping

Let's make your character move more realistically, by adding gravity and allowing them to jump.

+ You may have noticed that your character can walk off a platform into mid-air. Try to walk off of a platform and see what happens.
    
    ![screenshot](images/dodge-no-gravity.png)

+ To fix this, let's add gravity to your game. Create a new variable called `gravity`{:class="blockdata"}. You can hide this variable from your stage if you want to.
    
    ![screenshot](images/dodge-gravity.png)

+ Add this new code block, which sets the gravity to a negative number, and then uses this to repeatedly change your character's y-coordinate.
    
    ```blocks
        when flag clicked
        set [gravity v] to [-4]
        forever
            change y by (gravity)
        end
    ```

+ Click the flag, and then drag your character to the top of the stage. What happens? Does the gravity work as you expected?
    
    ![screenshot](images/dodge-gravity-drag.png)

+ Gravity shouldn't move your character through a platform or a ladder! Add an `if`{:class="blockcontrol"} block to your code, so that the gravity only works when your character is in mid-air. The gravity code should now look like this:
    
    ```blocks
        when flag clicked
        set [gravity v] to [-4]
        forever
            if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
                change y by (gravity)
            end
        end
    ```

+ Test the gravity again. Does your character stop when they are on a platform or a ladder? Can you walk off the edge of platforms to the level below?
    
    ![screenshot](images/dodge-gravity-test.png)

+ Let's also make your character jump when the player presses the space bar. One very easy way to do this is to move your character up a few times, using this code:
    
    ```blocks
        when [space v] key pressed
        repeat (10)
            change y by (4)
        end
    ```
    
    As gravity is constantly pushing your character down by 4 pixels, you need to choose a number greater than 4 in your `change y by (4)`{:class="blockmotion"} block. Change this number until you're happy with the height your character jumps.

+ If you test out this code, you'll notice that it works, but the movement isn't very smooth. To make jumping look smoother, you'll need to move your character by smaller and smaller amounts, until they're not jumping anymore.

+ To do this, create another variable called `jump height`{:class="blockdata"}. Again, you can hide this variable if you prefer.

+ Delete the jumping code you added to your character, and replace it with this code:
    
    ```blocks
        when [space v] key pressed
        set [jump height v] to [8]
        repeat until < (jump height) = [0] >
            change y by (jump height)
            change [jump height v] by (-0.5)
        end
    ```
    
    This code moves your character up by 8 pixels, then 7.5 pixels, then 7 pixels, and so on, until your character has finished jumping. This makes jumping look much smoother.

+ Change the starting value of your `jump height`{:class="blockdata"} variable and test it until you're happy with the height your character jumps.