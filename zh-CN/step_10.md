## 挑战：改进的重力

There's one other small bug in your game: gravity doesn't pull the character sprite downwards if **any** part of the sprite is touching a blue platform. 因此，即使是精灵头部接触平台，精灵也不会掉落！ You can test this yourself: make your character climb most of the way up a ladder, and then move the character sideways beneath a platform:

![截图](images/dodge-gravity-bug.png)

To fix the bug, you first need to give your character sprite new trousers that have a different colour (on **all** costumes).

![截图](images/dodge-trousers.png)

然后替换此代码块：

```blocks3
    < 碰到颜色 [#0000FF]? >
```

使用以下代码块：

```blocks3
    < 颜色 [#00FF00] 碰到 [#0000FF]? >
```

为确保错误已被修复，请在进行这些更改后测试游戏！