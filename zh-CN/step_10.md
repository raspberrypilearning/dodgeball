## 挑战：改进的重力

您的游戏中还有另外一个小错误：**，重力不会将角色精灵向下拉**精灵的一部分正在触摸蓝色平台。 因此，即使精灵头部接触平台，精灵也不会掉落！ 您可以自己进行测试：使角色大部分爬上梯子，然后将角色在平台下横向移动：

![screenshot](images/dodge-gravity-bug.png)

要修复该错误，您首先需要给角色精灵提供一条具有不同颜色的新裤子（在**全部**服饰）。

![screenshot](images/dodge-trousers.png)

然后替换此代码块：

```blocks3
    < touching color [#0000FF]? >
```

使用以下代码块：

```blocks3
    < color [#00FF00] is touching [#0000FF]? >
```

为确保已修复该错误，请在进行这些更改后测试游戏！