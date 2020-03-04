## 角色移动

首先创建一个可以左右移动并可以爬上梯子的角色。

\--- task \---

打开 'Dodgeball' Scratch 启动项目。

**在线编辑:** 在 [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){:target =“_ blank”} 打开初始项目。

如果您有一个 Scratch 帐户，您可以通过点击 **改编** 复制该项目。

**离线编辑:** 从 [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get) 下载初始项目，然后使用 Scratch 离线编辑器打开它。

\--- /task \---

该项目包含一个带有平台图案的背景：

![躲避球项目背景图案](images/dodge-background.png)

\--- task \---

选择一个新的精灵作为玩家将控制的角色，并将其添加到您的项目中。 最好选择带有走路动画的精灵，这样可以让它看起来更加自然

![选择一个精灵](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

向您的角色精灵添加代码块，以便玩家可以使用方向键来移动角色。 当玩家按下向右箭头时，角色应向右侧移动几步，然后换成下一个造型：

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
when flag clicked
forever
    if <key (right arrow v) pressed? > then
        point in direction (90 v)
        move (3) steps
        next costume
    end
end
```

\--- /task \---

\--- task \---

If your sprite doesn't fit, adjust its size.

![set sprite size so it fits](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Test out your character by clicking the flag and then holding down the right arrow key. Does your character move to the right? Does your character look like it is walking?

![screenshot](images/dodge-walking.png)

\--- /task \---

\--- task \---

Add code blocks to the character sprite's `forever`{:class="block3control"} loop so that it walks left if the left arrow key is pressed.

\--- hints \---

\--- hint \---

So that your character can move to the left, you'll need to add another `if`{:class="block3control"} block inside the `forever`{:class="block3control"} loop. In this new `if`{:class="block3control"} block, add code to make your character sprite `move`{:class="block3motion"} to the left.

\--- /hint \---

\--- hint \---

Copy the code you created to make the character walk to the right. Then set the `key pressed`{:class="block3sensing"} to the `left arrow`{:class="block3sensing"}, and change the `direction`{:class="block3motion"} to `-90`.

```blocks3
if <key (right arrow v) pressed? > then
    point in direction (90 v)
    move (3) steps
    next costume
end
```

\--- /hint \---

\--- hint \---

Your code should look like this now:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
when green flag clicked
forever 
  if <key (right arrow v) pressed?> then 
    point in direction (90 v)
    move (3) steps
    next costume
  end
  if <key (left arrow v) pressed?> then 
    point in direction (-90 v)
    move (3) steps
    next costume
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Test your new code to make sure that it works. Does your character turn upside-down when walking to the left?

![screenshot](images/dodge-upside-down.png)

If so, you can fix this by clicking on the **direction** of your character sprite, and then clicking on the left-right arrow.

![screenshot](images/dodge-left-right-annotated.png)

Or if you prefer, you can also fix the problem by adding this block to the start of your character's script:

```blocks3
set rotation style [left-right v]
```

\--- /task \---

\--- task \---

To climb a pink ladder, your character sprite should move a few steps upwards on the Stage whenever the up arrow is pressed **and** the character is touching the correct colour.

Add inside your character's `forever`{:class="block3control"} loop to `change`{:class="block3motion"} the character's `y` (vertical) position `if`{:class="block3control"} the `up arrow is pressed`{:class="block3sensing"} and the character is `touching the colour pink`{:class="block3sensing"}.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

\--- /task \---

\--- task \---

Test your code. Can you make the character climb the pink ladders and get to the end of the level?

![screenshot](images/dodge-test-character.png)

\--- /task \---