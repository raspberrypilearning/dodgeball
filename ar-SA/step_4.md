## الجاذبية و القفز

Now you're going to make your character move more realistically: you're going to add gravity to your game and give the character the ability to jump.

\--- task \---

In the game, move your character so that it walks off a platform. Do you see that it can walk into empty space?

![لقطة الشاشة](images/dodge-no-gravity.png)

\---/task--

\--- task \---

To fix this, add gravity to your game. To do this, create a new variable called `gravity`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

You can hide this variable from your Stage if you want to.

![لقطة الشاشة](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Add these new code blocks that set `gravity` to a negative number and use the value of `gravity` to repeatedly change your character's y-coordinate:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    عند نقر ⚑
اجعل [gravity v] مساوياً [-4]
كرر باستمرار 
  غيِّر الموضع ص بمقدار (gravity)
end
```

\--- /task \---

\--- task \---

Click the flag, and then drag your character to the top of the Stage. ماذا حدث؟ Does the gravity work as you expect?

![لقطة الشاشة](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Gravity shouldn't move the character sprite through a platform or a ladder! Add an `if`{:class="block3control"} block to your code to only let the gravity work when the character is in mid-air. The gravity code should then look like this:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    عند نقر ⚑
اجعل [gravity v] مساوياً [-4]
كرر باستمرار 
  إذا <ليس <<ملامس للون [#0000FF] ؟> أو <ملامس للون [#FF69B4] ؟>>> 
    غيِّر الموضع ص بمقدار (gravity)
  end
end
```

\--- /task \---

\--- task \---

Test the game again to see whether gravity works correctly now. Does your character sprite stop falling when it touches a platform or a ladder? Can you make the character walk off the edge of platforms and fall onto the level below?

![لقطة الشاشة](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Now add code to make your character jump whenever the player presses the <kbd>space</kbd> key. One very easy way to do this is to move your character up a few times:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    عند ضغط مفتاح [المسافة v]
كرِّر (10) مرة 
  غيِّر الموضع ص بمقدار (4)
end
```

Because gravity is constantly pushing your character down by 4 pixels, you need to choose a number greater than `4` in your `change y by (4)`{:class="block3motion"} block. Change the number until you're happy with the height the character jumps.

\--- /task \---

\--- task \---

Test out your code. Notice that the jumping movement isn't very smooth. To make jumping look smoother, you need to move your character sprite by smaller and smaller amounts, until it is not rising any higher.

\--- /task \---

\--- task \---

To do this, create a new variable called `jump height`{:class="block3variables"}. ويمكنك إخفاء هذا المتغير أيضًا إذا أردت.

\--- /task \---

\--- task \---

Delete the jumping code you added to your character sprite, and add this code instead:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    عند ضغط مفتاح [المسافة v]
اجعل [jump height v] مساوياً [8]
كرِّر حتى <(jump height) = [0]> 
  غيِّر الموضع ص بمقدار (jump height)
  غيِّر [jump height v] بمقدار (-0.5)
end
```

This code moves your character up by 8 pixels, then 7.5 pixels, then 7 pixels, and so on, until it does not rise any higher. وبذلك ستبدو القفزة اكثر سلاسة.

\--- /task \---

\--- task \---

Change the value of the `jump height`{:class="block3variables"} variable that is set before the `repeat`{:class="block3control"} starts. Then test your game.

Repeat these two steps until you're happy with how high the character jumps.

\--- /task \---