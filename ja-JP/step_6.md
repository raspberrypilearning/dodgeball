## ボールをよける

キャラクターは移動してジャンプできるので、キャラクターが避けなければならないボールを追加します。

--- task ---

新しいボールスプライトを作成。 好きなタイプのボールを選択できます。

![スクリーンショット](images/dodge-balls.png)

--- /task ---

--- task ---

キャラクターがジャンプできるようにボールスプライトのサイズを変更します。 キャラクターがボールを飛び越えて、ボールが正しいサイズかどうかをテストしてみてください。

![スクリーンショット](images/dodge-ball-resize.png)

--- /task ---

--- task ---

このコードをボールスプライトに追加します。

![ボールスプライト](images/ball_sprite.png)

```blocks3
when flag clicked
hide
forever 
  wait (3) seconds
  create clone of (自分自身 v)
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

このコードは、ボールスプライトの新しいクローンを3秒ごとに作成します。 新しいクローンはそれぞれ、一番上の床に沿って移動してから落ちます。

--- /task ---

--- task ---

フラグをクリックして、ゲームをテストします。

![スクリーンショット](images/dodge-ball-test.png)

--- /task ---

--- task ---

ボールスプライトにコードを追加して、3つのすべての床の間でそのクローンを移動します。

![スクリーンショット](images/dodge-ball-more-motion.png)

--- hints ---


--- hint ---

ボールスプライトクローンを最初の床に移動するために使用したコードブロックを繰り返します。 `x`{:class="block3motion"}、`y`{:class="block3motion"}を変更し、数を`繰り返し`{:class="block3control"}使用して、クローンが床に正しく追従するように変更する必要があります。

--- /hint ---

--- hint ---

これらが必要なブロックです。 必ず正しい順序で追加してください。

![ボールスプライト](images/ball_sprite.png)

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

ボールスプライトクローンのコードは次のようになります。

![ボールスプライト](images/ball_sprite.png)

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

ここで、コードブロックを追加して、キャラクターがボールにぶつかった場合にメッセージをブロードキャスト(送信) します！

このコードをボールスプライトに追加します。

![ボールスプライト](images/ball_sprite.png)

```blocks3
when I start as a clone
forever 
  if <touching (歩いているピコ v) ?> then 
    broadcast (ヒット v)
  end
end
```

--- /task ---

--- task ---

最後に、キャラクタースプライトにコードブロックを追加して、`ヒット`メッセージを受け取ったときに開始位置に戻るようにします:

![歩いているピコスプライト](images/pico_walking_sprite.png)

```blocks3
when I receive [ヒット v]
point in direction (90)
go to x: (-210) y: (-120)
```

--- /task ---

--- task ---

コードをテストしましょう。 ボールに触れた後、キャラクターが最初に戻るかどうかを確認します。

--- /task ---