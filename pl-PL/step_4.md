## Grawitacja i skakanie

Teraz sprawisz, że Twoja postać będzie poruszać się bardziej realistycznie: dodasz grawitację do swojej gry i dasz postaci umiejętność skakania.

\--- task \---

W grze poruszaj swoją postacią tak, aby zeszła z platformy. Czy widzisz, że może wejść w puste miejsce?

![zrzut ekranu](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

Aby to naprawić, dodaj grawitację do swojej gry. Żeby to zrobić, utwórz nową zmienną o nazwie `grawitacja`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Możesz ukryć tą zmienną na scenie jeśli chcesz.

![zrzut ekranu](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Add these new code blocks that set `gravity` to a negative number and use the value of `gravity` to repeatedly change your character's y-coordinate:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    kiedy kliknięto flagę
    ustaw [gravity v] na [-4]
    zawsze
        zmień y o (grawitacja)
    end
```

\--- /task \---

\--- task \---

Click the flag, and then drag your character to the top of the Stage. What happens? Does the gravity work as you expect?

![zrzut ekranu](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Gravity shouldn't move the character sprite through a platform or a ladder! Add an `if`{:class="block3control"} block to your code to only let the gravity work when the character is in mid-air. The gravity code should then look like this:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    kiedy kliknięto flagę
        ustaw [grawitacja v] na [-4]
        zawsze
            jeżeli < nie < <touching color [#0000FF]?> lub <touching color [#FF69B4]?> > > to
                zmień y o (grawitacja)
            end
        end
```

\--- /task \---

\--- task \---

Test the game again to see whether gravity works correctly now. Does your character sprite stop falling when it touches a platform or a ladder? Can you make the character walk off the edge of platforms and fall onto the level below?

![zrzut ekranu](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Now add code to make your character jump whenever the player presses the <kbd>space</kbd> key. One very easy way to do this is to move your character up a few times:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    kiedy klawisz [spacja v] naciśnięty
        powtórz (10) razy
            zmień y o (4)
        end
```

Because gravity is constantly pushing your character down by 4 pixels, you need to choose a number greater than `4` in your `change y by (4)`{:class="block3motion"} block. Change the number until you're happy with the height the character jumps.

\--- /task \---

\--- task \---

Test out your code. Notice that the jumping movement isn't very smooth. To make jumping look smoother, you need to move your character sprite by smaller and smaller amounts, until it is not rising any higher.

\--- /task \---

\--- task \---

To do this, create a new variable called `jump height`{:class="block3variables"}. Ponownie, jeśli chcesz możesz ukryć tę zmienną.

\--- /task \---

\--- task \---

Delete the jumping code you added to your character sprite, and add this code instead:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    kiedy klawisz [spacja v] naciśnięty
        ustaw [wysokość skoku v] na [8]
        powtarzaj aż < (wysokość skoku) = [0] >
            zmień y o (wysokość skoku)
            zmień [wysokość skoku v] o (-0,5)
        end
```

This code moves your character up by 8 pixels, then 7.5 pixels, then 7 pixels, and so on, until it does not rise any higher. To uczyni wygląd skoków bardziej płynnym.

\--- /task \---

\--- task \---

Change the value of the `jump height`{:class="block3variables"} variable that is set before the `repeat`{:class="block3control"} starts. Then test your game.

Repeat these two steps until you're happy with how high the character jumps.

\--- /task \---