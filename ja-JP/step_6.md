## ボールをよける

キャラクターは移動してジャンプできるので、キャラクターが避けなければならないボールを追加します。

\--- task \---

新しいボールスプライトを作成。 好きなタイプのボールを選択できます。

![スクリーンショット](images/dodge-balls.png)

\--- /task \---

\--- task \---

キャラクターがジャンプできるようにボールスプライトのサイズを変更します。 キャラクターがボールを飛び越えて、ボールが正しいサイズかどうかをテストしてみてください。

![スクリーンショット](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

このコードをボールスプライトに追加します。

![ball sprite](images/ball_sprite.png)

```blocks3
グリーンフラグが押されたとき
隠す
ずっと
  (3) 秒間待つ
  (自分自身 v) のクローンを作る
終了
```

```blocks3
クローンされたとき
x座標を(160) y座標を (160) にする
表示する
(22) 回繰り返す
  y座標を(-4) ずつ変える
終了
(170) 回繰り返す 
  x座標を (-2) ずつ変える
  反時計回りに(6) 度回す
終了
(30) 回繰り返す 
  y座標を(-4) ずつ変える
終了
このクローンを削除する
```

このコードは、ボールスプライトの新しいクローンを3秒ごとに作成します。 新しいクローンはそれぞれ、一番上のプラットフォームに沿って移動してから落ちます。

\--- /task \---

\--- task \---

フラグをクリックして、ゲームをテストします。

![スクリーンショット](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

ボールスプライトにコードを追加して、3つのすべてのプラットフォーム間でそのクローンを移動します。

![スクリーンショット](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Repeat the code blocks you used to move the ball sprite clone across the first platform. `x` {:class="block3motion"}、`y ` {:class="block3motion"}を変更し、数を`繰り返し` {:class="block3control"}使用して、クローンがプラットフォームに正しく追従するように変更する必要があります。

\--- /hint \---

\--- hint \---

These are the blocks you need. Make sure you add them in the correct order.

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

\--- /ヒント \---

\--- hint \---

The code for your ball sprite clones should look like this:

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

\--- /ヒント \---

\--- /ヒント \---

\--- /task \---

\--- task \---

Now add some code blocks to broadcast (send) a message if your character gets hit by a ball!

Add this code to your ball sprite:

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

Finally, add code blocks to your character sprite to make it move back to its starting position when it receives the `hit` message:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Test out your code. Check whether the character moves back to the start after touching a ball.

\--- /task \---