## 重力和跳跃

现在，您将会把角色的移动做得更加逼真：为游戏增加重力，并使角色具有跳跃的能力。

\--- task \---

在游戏中，移动您的角色，使其离开平台。 您看到它可以进入空白空间吗？

![screenshot](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

To fix this, add gravity to your game. To do this, create a new variable called `gravity`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

You can hide this variable from your Stage if you want to.

![screenshot](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Add these new code blocks that set `gravity` to a negative number and use the value of `gravity` to repeatedly change your character's y-coordinate:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        change y by (gravity)
    end
```

\--- /task \---

\--- task \---

Click the flag, and then drag your character to the top of the Stage. What happens? Does the gravity work as you expect?

![screenshot](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Gravity shouldn't move the character sprite through a platform or a ladder! Add an `if`{:class="block3control"} block to your code to only let the gravity work when the character is in mid-air. The gravity code should then look like this:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
            change y by (gravity)
        end
    end
```

\--- /task \---

\--- task \---

Test the game again to see whether gravity works correctly now. Does your character sprite stop falling when it touches a platform or a ladder? Can you make the character walk off the edge of platforms and fall onto the level below?

![screenshot](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Now add code to make your character jump whenever the player presses the <kbd>space</kbd> key. One very easy way to do this is to move your character up a few times:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    repeat (10)
        change y by (4)
    end
```

Because gravity is constantly pushing your character down by 4 pixels, you need to choose a number greater than `4` in your `change y by (4)`{:class="block3motion"} block. Change the number until you're happy with the height the character jumps.

\--- /task \---

\--- task \---

Test out your code. Notice that the jumping movement isn't very smooth. To make jumping look smoother, you need to move your character sprite by smaller and smaller amounts, until it is not rising any higher.

\--- /task \---

\--- task \---

To do this, create a new variable called `jump height`{:class="block3variables"}. Again, you can hide this variable if you prefer.

\--- /task \---

\--- task \---

Delete the jumping code you added to your character sprite, and add this code instead:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    set [jump height v] to [8]
    repeat until < (jump height) = [0] >
        change y by (jump height)
        change [jump height v] by (-0.5)
    end
```

This code moves your character up by 8 pixels, then 7.5 pixels, then 7 pixels, and so on, until it does not rise any higher. This makes jumping look much smoother.

\--- /task \---

\--- task \---

Change the value of the `jump height`{:class="block3variables"} variable that is set before the `repeat`{:class="block3control"} starts. Then test your game.

Repeat these two steps until you're happy with how high the character jumps.

\--- /task \---