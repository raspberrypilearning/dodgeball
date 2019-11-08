## Gravity and jumping

次に、キャラクターをよりリアルに動かします: ゲームに重力を加えて、キャラクターにジャンプする能力を与えます。

\--- task \---

ゲーム内でキャラクターを動かして、プラットフォームから離れるようにします。 空の空間に足を踏み入れることができると思いますか？

![スクリーンショット](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

これを修正するには、ゲームに重力を追加します。 これを行うには、` 重力` {:class="block3variables"}という新しい変数を作成します。

[[[generic-scratch3-add-variable]]]

必要に応じて、この変数をステージから非表示にできます。

![スクリーンショット](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

`重力`にマイナスの値にし、この`重力`の値を使ってキャラクターのy座標を繰り返し変更する新しいコードブロックを追加します:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        change y by (gravity)
    end
```

\--- /task \---

\--- task \---

フラグをクリックし、キャラクターをステージの上部にドラッグします。 何が起こった？ 重力は期待どおりに機能しますか？

![スクリーンショット](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

重力は、キャラクタースプライトをプラットフォームやはしごの中では動かしてはいけません！ ` もし` {:class="block3control"}ブロックをコードに追加し、キャラクターが空中にあるときにのみ重力が機能するようにします。 重力コードは次のようになります。

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
            change y by (gravity)
        end
    end
```

\--- /task \---

\--- task \---

ゲームをもう一度テストして、重力が正しく機能するかどうかを確認してください。 キャラクタースプライトがプラットフォームまたははしごに触れると、落下しなくなりますか？ キャラクターをプラットフォームの端から歩いて落とし、下のレベルに落とすことができますか？

![スクリーンショット](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

プレーヤーが<kbd>スペース</kbd>キーを押すたびにキャラクターをジャンプさせるコードを追加します これを行う非常に簡単な方法の1つは、キャラクターを数回上に移動することです。

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    [スペース v] キーが押されたとき
    (10) 回繰り返す
        y座標を (4) ずつ変える
    終了
```

重力がキャラクターを常に4ピクセル押し下げているため、y座標で`(4) ずつ変わる ` {:class="block3motion"} ブロックの中で、` 4 `より大きい数を選択する必要があります 。 キャラクターがジャンプする高さに満足するまで数を変更します。

\--- /task \---

\--- task \---

コードをテストしましょう。 Notice that the jumping movement isn't very smooth. To make jumping look smoother, you need to move your character sprite by smaller and smaller amounts, until it is not rising any higher.

\--- /task \---

\--- task \---

To do this, create a new variable called `jump height`{:class="block3variables"}. Again, you can hide this variable if you prefer.

\--- /task \---

\--- task \---

Delete the jumping code you added to your character sprite, and add this code instead:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    set [jump height v] to [8]
    repeat until < (jump height) = [0] >
        change y by (jump height)
        change [jump height v] by (-0.5)
    end
```

This code moves your character up by 8 pixels, then 7.5 pixels, then 7 pixels, and so on, until it does not rise any higher. This makes jumping look much smoother.

\--- /task \---

\--- task \---

Change the value of the `jump height`{:class="block3variables"} variable that is set before the `repeat`{:class="block3control"} starts. Then test your game.

Repeat these two steps until you're happy with how high the character jumps.

\--- /task \---