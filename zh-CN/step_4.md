## 重力和跳跃

现在，您将会把角色的移动做得更加逼真：为游戏增加重力，并使角色具有跳跃的能力。

\--- task \---

在游戏中，移动您的角色，使其离开平台。 您看到它可以走到了空白的地方吗？

![截图](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

要解决这个问题，需要在游戏中添加重力 创建一个新的名为 `gravity`{:class="block3variables"} 的变量

[[[generic-scratch3-add-variable]]]

您可以根据需要在舞台中隐藏此变量。

![截图](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

添加下面这些设置 `gravity` 为负数的代码块，并使用 ` gravity` 的值反复更改角色的 y 坐标：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    当 标志 被点击
    将 [gravity v] 设置为 [-4]
    重复执行
        将 y 坐标增加 (gravity)
    结束
```

\--- /task \---

\--- task \---

单击标志，然后将您的角色拖动到舞台的顶部。 发生了什么? 这个重力效果是不是你想要的呢？

![截图](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Gravity shouldn't move the character sprite through a platform or a ladder! 添加一个 `如果`{:class="block3control"} 积木块到你的代码中，只有当角色处于空中时才让重力起作用。 重力代码应如下所示：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    当 标志 被点击
    将 [gravity v] 设置为 [-4]
    重复执行
        如果 < < <touching color [#0000FF]?> 或 <touching color [#FF69B4]?> > 不成立 > 那么
            将 y 坐标增加 (gravity)
        结束
    结束
```

\--- /task \---

\--- task \---

再次测试游戏，看看现在重力是否正常工作。 当角色精灵接触到平台或梯子时，它会不会停止下落？ 您可以使角色走出平台边缘并掉到下面的平台吗？

![截图](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

现在添加代码以使您的角色在玩家按下<kbd>空格</kbd>键时跳起来。 一种非常简单的方法是将角色向上移动几次：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    当按下 [空格 v] 键
    重复执行 (10) 次
        将 y 坐标增加 (4)
    结束
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