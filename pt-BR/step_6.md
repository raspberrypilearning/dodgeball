## Esquivando das bolas

Agora que você tem seu personagem se movendo, vamos adicionar algumas bolas para seu personagem evitar.

+ Create a new ball sprite. You can choose any type of ball you like.
    
    ![screenshot](images/dodge-balls.png)

+ Resize your ball, so that your character can jump over it. Try jumping over the ball to test it.
    
    ![screenshot](images/dodge-ball-resize.png)

+ Add this code to your ball:
    
    ![screenshot](images/dodge-ball-motion.png)
    
    This code creates a new ball clone every 3 seconds. Each new clone moves along the top platform.

+ Click the flag to test this out.
    
    ![screenshot](images/dodge-ball-test.png)

+ Add more code to your ball sprite, so that they move across all 3 platforms.
    
    ![screenshot](images/dodge-ball-more-motion.png)

+ Finally, you'll need code for when your character gets hit by a ball! Add this code to your ball sprite:
    
    ```blocks
        when I start as a clone
        forever
            if < touching [Pico walking v]? > then
                broadcast [hit v]
            end
        end
    ```

+ You'll also need to add code to your character, to move back to the start when they're hit:
    
    ```blocks
        when I receive [hit v]
        point in direction (90 v)
        go to x: (-210) y: (-120)
    ```

+ Test out your character and see if they go back to the start when they've been hit by a ball.