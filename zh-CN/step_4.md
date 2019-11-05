## 重力和跳跃

现在，您将使角色更加逼真地移动：将为游戏增加重力，并使角色具有跳跃的能力。

\--- task \---

在游戏中，移动您的角色，使其离开平台。 您看到它可以进入空白空间吗？

![screenshot](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

要解决此问题，请在游戏中添加重力。 创建一个新的名为`gravity`{:class="block3variables"}的变量

[[[generic-scratch3-add-variable]]]

您可以根据需要在舞台中隐藏此变量。

![screenshot](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

添加这些新的设置`重力的代码块`为负数，并使用` gravity的值`重复更改角色的y坐标：

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

单击标志，然后将您的角色拖动到舞台的顶部。 发生了什么? 引力是否如您所愿？

![screenshot](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

重力不应该使角色精灵穿过平台或梯子！ 添加` ` {：class =“ block3control”}阻止您的代码，仅在角色处于空中时才使重力起作用。 重力代码应如下所示：

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

再次测试游戏，看看现在重力是否正常工作。 当角色精灵接触平台或梯子时，它会不会停止下落？ 您可以使角色走出平台边缘并掉入下面的水平面吗？

![screenshot](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

现在添加代码以使您的角色在玩家按下<kbd>空格时跳转</kbd>键。 一种非常简单的方法是将角色向上移动几次：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    repeat (10)
        change y by (4)
    end
```

由于重力不断将您的角色向下推4个像素，因此您需要选择一个大于` 4的数字`在您的`更改y中将（4） ` {：class =“ block3motion”}块。 更改数字，直到您对角色跳跃的高度满意为止。

\--- /task \---

\--- task \---

测试您的代码。 请注意，跳跃动作不是很平滑。 为了使跳跃看起来更平滑，您需要将角色精灵移动的越来越少，直到不再升高为止。

\--- /task \---

\--- task \---

为此，请创建一个名为` jump height的新变量。 ` {：class =“ block3variables”}。 同样，您可以根据需要隐藏此变量。

\--- /task \---

\--- task \---

删除添加到角色精灵中的跳转代码，然后添加以下代码：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    set [jump height v] to [8]
    repeat until < (jump height) = [0] >
        change y by (jump height)
        change [jump height v] by (-0.5)
    end
```

这段代码将您的字符上移8个像素，然后是7.5个像素，然后是7个像素，依此类推，直到它不再升高为止。 这使跳跃看起来更加平滑。

\--- /task \---

\--- task \---

更改`跳跃高度的值` {：class =“ block3variables”}变量，该变量在`重复之前设置` {：class =“ block3control”}开始。 然后测试您的游戏。

重复这两个步骤，直到您对角色跳跃的高度感到满意为止。

\--- /task \---