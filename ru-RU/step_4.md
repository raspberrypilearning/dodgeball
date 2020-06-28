## Гравитация и прыжки

Теперь ты сделаешь так, чтобы твой персонаж мог двигаться более реалистично: добавишь гравитацию и дашь персонажу возможность прыгать.

\--- task \---

Перемести своего персонажа так, чтобы он сходил с платформы. Видишь, что он идет по пустому пространству?

![снимок экрана](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

Чтобы это исправить, добавь гравитацию в игру. Создай новую переменную с именем `гравитация`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Ты можешь скрыть эту переменную со Сцены.

![снимок экрана](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Добавь эти новые блоки кода, которые задают отрицательное число `гравитации` и с помощью значения `гравитации` многократно меняй y-координату своего персонажа:

![спрайт Пико ходит](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        change y by (gravity)
    end
```

\--- /task \---

\--- task \---

Нажми на флаг, а затем перетащи своего персонажа на вершину Сцены. Что происходит? Гравитация работает так, как ты ожидал?

![снимок экрана](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Гравитация не должна перемещать спрайт персонажа на платформе или лестнице! Добавь блок `если`{:class="block3control"} в свой код, чтобы гравитация работала только тогда, когда персонаж находится в воздухе. Код гравитации должен выглядеть следующим образом:

![спрайт Пико ходит](images/pico_walking_sprite.png)

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