## Gravity and jumping

次に、キャラクターをよりリアルに動かします: ゲームに重力を加えて、キャラクターにジャンプする能力を与えます。

\--- task \---

ゲーム内でキャラクターを動かして、プラットフォームから離れるようにします。 空の空間に足を踏み入れることができると思いますか？

![スクリーンショット](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

これを修正するには、ゲームに重力を追加します。 これを行うには、` 重力` {:class="block3variables"}という新しい変数を作成します。

[[[generic-scratch3-add-variable]]]

必要に応じて、この変数をステージから非表示にできます。

![スクリーンショット](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

`重力`にマイナスの値にし、この`重力`の値を使ってキャラクターのy座標を繰り返し変更する新しいコードブロックを追加します:

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

フラグをクリックし、キャラクターをステージの上部にドラッグします。 何が起こった？ Does the gravity work as you expect?

![スクリーンショット](images/dodge-gravity-drag.png)

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

![スクリーンショット](images/dodge-gravity-test.png)

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