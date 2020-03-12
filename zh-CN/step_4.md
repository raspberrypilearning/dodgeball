## 重力和跳跃

现在，您将会把角色的移动做得更加逼真：为游戏增加重力，并使角色具有跳跃的能力。

--- task ---

在游戏中，移动您的角色，使其离开平台。 您看到它可以走到了空白的地方吗？

![截图](images/dodge-no-gravity.png)

--- /task ---

--- task ---

要解决这个问题，需要在游戏中添加重力 创建一个新的名为 `重力`{:class="block3variables"} 的变量

[[[generic-scratch3-add-variable]]]

您可以根据需要在舞台中隐藏此变量。

![截图](images/dodge-gravity-annotated.png)

--- /task ---

--- task ---

添加下面这些设置 `重力` 为负数的代码块，并使用 `重力` 的值反复更改角色的 y 坐标：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
	set [重力 v] to [-4]
	forever
		change y by (重力)
	end
```

--- /task ---

--- task ---

单击标志，然后将您的角色拖动到舞台的顶部。 发生了什么? 这个重力效果是不是你想要的呢？

![截图](images/dodge-gravity-drag.png)

--- /task ---

--- task ---

重力不应该使角色精灵穿过平台或梯子！ 添加一个 `如果`{:class="block3control"} 积木块到你的代码中，只有当角色处于空中时才让重力起作用。 重力代码应如下所示：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
	set [重力 v] to [-4]
	forever
		if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
			change y by (重力)
		end
	end
```

--- /task ---

--- task ---

再次测试游戏，看看现在重力是否正常工作。 当角色精灵接触到平台或梯子时，它会不会停止下落？ 您可以使角色走出平台边缘并掉到下面的平台吗？

![截图](images/dodge-gravity-test.png)

--- /task ---

--- task ---

现在添加代码以使您的角色在玩家按下<kbd>空格</kbd>键时跳起来。 一种非常简单的方法是将角色向上移动几次：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
	repeat (10)
		change y by (4)
	end
```

由于重力不断将您的角色向下推4个像素，因此您需要在 `将 y 坐标增加 (4)`{:class="block3motion"} 的积木块中选择一个大于 `4` 的数字。 更改数字，直到您对角色跳跃的高度满意为止。

--- /task ---

--- task ---

测试您的代码。 注意到跳跃动作不是很平滑。 为了使跳跃看起来更平滑，需要把角色精灵上升的幅度调整的越来越小，直到不再升高为止。

--- /task ---

--- task ---

因此需要再创建一个名为 `jump height`{:class="block3variables"} 的新变量。 同样的，您可以根据需要隐藏此变量。

--- /task ---

--- task ---

删除已经添加到角色精灵中的跳跃部分的代码，然后添加以下代码：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
	set [jump height v] to [8]
	repeat until < (jump height) = [0] >
		change y by (jump height)
		change [jump height v] by (-0.5)
	end
```

这段代码将您的角色先上移 8 个像素，然后再上移 7.5 个像素，然后再上移 7 个像素，依此类推，直到它不再升高为止。 这样就使得跳跃看起来更加平滑。

--- /task ---

--- task ---

记得要把 设置 `jump height`{:class="block3variables"} 积木块放在变量，该变量在 `重复执行`{:class="block3control"} 的积木块前面。 然后测试您的游戏。

重复这两个步骤，直到您对角色跳跃的高度感到满意为止。

--- /task ---