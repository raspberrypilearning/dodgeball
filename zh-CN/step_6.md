## 躲避球

您的角色现在可以移动和跳跃，因此是时候添加一些角色必须避免的球了。

\--- task \---

创建一个新的球精灵。 你可以选择你喜欢的任何类型的球。

![screenshot](images/dodge-balls.png)

\--- /task \---

\--- task \---

调整球形精灵的大小，以便角色可以越过球形精灵。 尝试使角色跳过球以测试球的尺寸是否正确。

![screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

将下面的代码添加到球精灵角色中：

![ball sprite](images/ball_sprite.png)

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

此代码每三秒钟创建一个新的球形精灵克隆。 每个新克隆都沿着顶部平台移动，然后掉落。

\--- /task \---

\--- task \---

单击标志以测试游戏。

![screenshot](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

向您的球形精灵添加更多代码，以便其副本在所有三个平台上移动。

![screenshot](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

重复您用来在第一个平台上移动球形精灵克隆的代码块。 您需要更改` x ` {：class =“ block3motion”}，` y ` {：class =“ block3motion”}，然后`重复` {：class =“ block3control”}数字，以便克隆正确遵循平台。

\--- /hint \---

\--- hint \---

以下是你需要的代码块： 确保以正确的顺序添加它们。

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

\--- /hint \---

\--- hint \---

您的球精灵克隆的代码应如下所示：

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

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

现在，如果您的角色被球击中，请添加一些代码块以广播（发送）消息！

将下面的代码添加到球精灵角色中：

![ball sprite](images/ball_sprite.png)

```blocks3
    when I start as a clone
    forever
        if < touching (Pico walking v)? > then
            broadcast (hit v)
        end
    end
```

\--- /task \---

\--- task \---

最后，在您的角色精灵上添加代码块，以使其在收到`命中时返回其初始位置`信息：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

测试您的代码。 触摸球后，检查角色是否回到起始位置。

\--- /task \---