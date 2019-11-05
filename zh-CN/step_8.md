## 激光！

为了让您的游戏更难完成，您将添加激光！

\--- task \---

在游戏中添加新的精灵，并将其命名为` laser ` 。 它应该有两种造型：一种叫做“开”，另一种叫做“关”。

![screenshot](images/dodge-lasers-costume1.png)

![screenshot](images/dodge-lasers-costume1.png)

\--- /task \---

\--- task \---

将新的激光精灵放置在两个平台之间。

![screenshot](images/dodge-lasers-position.png)

\--- /task \---

\--- task \---

向您的激光精灵添加代码，以使其在其两个造型之间切换。

![laser sprite](images/laser_sprite.png)

```blocks3
    when flag clicked
    forever
        switch costume to (on v)
        wait (2) seconds
        switch costume to (off v)
        wait (2) seconds
    end
```

如果愿意，可以更改上面显示的代码，以便精灵`等待` {：class =“ block3control”} `随机` {：class =“ block3operators”}两次造型更换之间的时间间隔。

\--- /task \---

\--- task \---

最后，向您的激光精灵添加代码，以便激光精灵碰到角色精灵时会广播“ hit”消息。

\--- hints \---

\--- hint \---

该代码应与您添加到球精灵中的代码非常相似。

\--- /hint \---

\--- hint \---

复制您添加到球精灵的代码，以使该精灵`广播“命中” ` {：class =“ block3control”}当它`碰到您的角色时` {：class =“ block3sensing”}。

\--- /hint \---

\--- hint \---

这是您应该添加的代码：

![laser sprite](images/laser_sprite.png)

```blocks3
when green flag clicked
forever 
  if <touching (Pico walking v) ?> then 
    broadcast (hit v)
  end
end
```

\--- /hint \---

\--- /hints \---

您无需在角色精灵上添加任何额外的代码，因为角色精灵在接收到`广播“ hit”后就已经知道该怎么做了。 ` {：class =“ block3control”}！

\--- /task \---

\--- task \---

测试您的游戏，看看是否可以将角色移过激光。 If the laser is too easy or too hard to avoid, change the `wait`{:class="block3control"} times in the code for the laser sprite.

\--- /task \---