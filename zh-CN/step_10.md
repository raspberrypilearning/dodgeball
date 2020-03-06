## 挑战：改进的重力

您的游戏中还有另外一个小 bug: 如果游戏精灵的 **任何** 部位接触到了蓝色的平台，那么角色精灵将不会下落 因此，即使是精灵头部接触平台，精灵也不会掉落！ 您可以测试一下：让角色精灵爬上梯子，但不是完全爬上梯子，然后将角色精灵移动到平台下方:

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