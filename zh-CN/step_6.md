## 躲避球

您的角色现在已经可以移动和跳跃了，是时候添加一些躲避球了。

--- task ---

创建一个新的小球精灵。 您可以选择任何您喜欢的球。

![截图](images/dodge-balls.png)

--- /task ---

--- task ---

调整球形精灵的大小，以便角色可以跳过它。 尝试使角色跳过球以测试球的大小是否合适。

![截图](images/dodge-ball-resize.png)

--- /task ---

--- task ---

将下面的代码添加到小球精灵中：

![小球精灵](images/ball_sprite.png)

```blocks3
when green flag clicked
hide
forever 
  wait (3) seconds
  create clone of (myself v)
end
```

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
delete this clone
```

此代码每三秒钟创建一个新的小球精灵克隆。 每个新克隆都沿着顶部平台移动，然后掉落。

--- /task ---

--- task ---

单击标志以测试游戏。

![截图](images/dodge-ball-test.png)

--- /task ---

--- task ---

向您的小球精灵添加更多代码，以便其克隆体在所有三个平台上移动。

![截图](images/dodge-ball-more-motion.png)

--- hints ---


--- hint ---

重复刚才在第一个平台上移动小球精灵克隆体的代码块。 您需要更改 `x`{:class="block3motion"}，`y`{:class="block3motion"}，和 `重复执行`{:class="block3control"} 次数，以便克隆体能够在平台上正确移动。

--- /hint ---

--- hint ---

以下是您需要的代码块： 确保以正确的顺序添加它们。

![ball sprite](images/ball_sprite.png)

```blocks3
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end

repeat (180) 
  change x by (2)
  turn cw (6) degrees
end

repeat (30) 
  change y by (-4)
end
```

--- /hint ---

--- hint ---

您的小球精灵克隆体的代码应如下所示：

![ball sprite](images/ball_sprite.png)

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (180) 
  change x by (2)
  turn cw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
delete this clone
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

现在，如果您的角色被球击中，请添加一些代码块以广播 (发送) 消息！

将下面的代码添加到小球精灵角色中：

![ball sprite](images/ball_sprite.png)

```blocks3
  when I start as a clone
	forever
		if < touching (Pico walking v)? > then
			broadcast (hit v)
		end
	end
```

--- /task ---

--- task ---

最后，在您的角色精灵添加代码块，以使其在收到 `hit` 消息时返回起点位置：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
  when I receive [hit v]
	point in direction (90)
	go to x: (-210) y: (-120)
```

--- /task ---

--- task ---

测试您的代码。 检查角色在碰到小球后是否回到起点位置。

--- /task ---