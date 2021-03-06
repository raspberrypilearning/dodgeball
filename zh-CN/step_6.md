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
当 ⚑ 被点击
隐藏
重复执行 
  等待 (3) 秒
  克隆 (自己 v)
end
```

```blocks3
当作为克隆体启动时
移到 x: (160) y: (160)
显示
重复执行 (22) 次 
  将y坐标增加 (-4)
end
重复执行 (170) 次 
  将x坐标增加 (-2)
  左转 ↺ (6) 度
end
重复执行 (30) 次 
  将y坐标增加 (-4)
end
删除此克隆体
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
重复执行 (170) 次 
  将x坐标增加 (-2)
  左转 ↺ (6) 度
end

重复执行 (180) 次 
  将x坐标增加 (2)
  右转 ↻ (6) 度
end

重复执行 (30) 次 
  将y坐标增加 (-4)
end
```

--- /hint ---

--- hint ---

您的小球精灵克隆体的代码应如下所示：

![ball sprite](images/ball_sprite.png)

```blocks3
当作为克隆体启动时
移到 x: (160) y: (160)
显示
重复执行 (22) 次 
  将y坐标增加 (-4)
end
重复执行 (170) 次 
  将x坐标增加 (-2)
  左转 ↺ (6) 度
end
重复执行 (30) 次 
  将y坐标增加 (-4)
end
重复执行 (180) 次 
  将x坐标增加 (2)
  右转 ↻ (6) 度
end
重复执行 (30) 次 
  将y坐标增加 (-4)
end
重复执行 (170) 次 
  将x坐标增加 (-2)
  左转 ↺ (6) 度
end
删除此克隆体
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

现在，如果您的角色被球击中，请添加一些代码块以广播 (发送) 消息！

将下面的代码添加到小球精灵角色中：

![ball sprite](images/ball_sprite.png)

```blocks3
当作为克隆体启动时
重复执行 
  如果 <碰到 (Pico walking v) ?> 那么 
    广播 (打 v)
  end
end
```

--- /task ---

--- task ---

最后，在您的角色精灵添加代码块，以使其在收到 `打` 消息时返回起点位置：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
  当接收到 [打 v]
  面向 (90) 方向
  移到 x: (-210) y: (-120)
```

--- /task ---

--- task ---

测试您的代码。 检查角色在碰到小球后是否回到起点位置。

--- /task ---