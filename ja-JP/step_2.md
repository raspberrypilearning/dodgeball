## キャラクターの動き

左右に移動でき、はしごを登ることができるキャラクターを作成することから始めます。

\--- task \---

「ドッジボール」 スクラッチスタータープロジェクトを開きます。

**Online:** open the starter project at [rpf.io/dodgeball-on](https://rpf.io/dodgeball-on){:target="_blank"}.

スクラッチアカウントをお持ちの場合は**リミックス**をクリックしてコピーを作成できます。

**Offline:** download the starter project from [rpf.io/p/en/dodgeball-get](https://rpf.io/p/en/dodgeball-get) and then open it using the offline editor.

\--- /task \---

プロジェクトには、床のある背景が含まれています。

![ドッジボールプロジェクトの背景](images/dodge-background.png)

\--- task \---

プレーヤーが制御するキャラクターとして新しいスプライトを選択し、プロジェクトに追加します。 複数のコスチュームを持つスプライトを選択すると、歩いているように見せることができます。

![スプライトを選ぶ](images/dodge-characters.png)

[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

プレイヤーが矢印キーでキャラクターを移動できるように、キャラクタースプライトにコードブロックを追加します。 プレイヤーが右矢印を押すと、キャラクターは右を向き、数歩移動して次のコスチュームに変更します。

![ピコウォーキングスプライト](images/pico_walking_sprite.png)

```blocks3
⚑ が押されたとき
ずっと 
  もし <(右向き矢印 v) キーが押された> なら
  end
end > なら
(90 v) 度に向ける
(3) 歩動かす
次のコスチュームにする
end
end
```

\--- /task \---

\--- task \---

スプライトが収まらない場合は、サイズを調整します。

![収まるようにスプライトのサイズを設定します](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

フラグをクリックしてから右矢印キーを押して、キャラクターをテストします。 キャラクターは右に移動しますか？ キャラクターは歩いているように見えますか？

![スクリーンショット](images/dodge-walking.png)

\--- /task \---

\--- task \---

キャラクタースプライトに`ずっと` {:class="block3control"}ループ加えたので、左矢印キーが押されると左に移動します。

\--- hints \---

\--- hint \---

キャラクターが左に移動できるようにするには、 ` forever` {:class="block3control"}ループの内側に、別の` if`{:class="block3control"}ブロックを追加する必要があります。 この新しい` if ` {:class="block3control"}ブロックの中で、キャラクタースプライトを左側へ`移動`{:class="block3motion"}するようにコードを追加します。

\--- /hint \---

\--- hint \---

キャラクターが右に歩くよう作成したコードをコピーします。 さらに、`左向き矢印` {:class="block3sensing"}の`キーが押された` {:class="block3sensing"}ら、`向き` {:class="block3motion"} を` -90 `度に変更するするようにセットします。

```blocks3
もし < (右向き矢印 v) キーが押された > なら
    (90 v) 度に向ける
    (3) 歩動かす
    次のコスチュームにする
end
```

\--- /hint \---

\--- hint \---

コードは以下のようになります:

![ピコウォーキングスプライト](images/pico_walking_sprite.png)

```blocks3
⚑ が押されたとき
ずっと 
  もし <key (right arrow v) pressed?> なら 
    (90 v) 度に向ける
    (3) 歩動かす
    次のコスチュームにする
  end
  もし <key (left arrow v) pressed?> なら 
    (-90 v) 度に向ける
    (3) 歩動かす
    次のコスチュームにする
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

新しいコードをテストして、動作することを確認します。 キャラクターは左に歩いているときに逆さまになりますか？

![スクリーンショット](images/dodge-upside-down.png)

その場合、キャラクタースプライトの**向き**をクリックして、さらに左右反転をクリックして修正できます

![スクリーンショット](images/dodge-left-right-annotated.png)

または、必要に応じて、このブロックをキャラクターのスクリプトの先頭に追加して問題を修正することもできます。

```blocks3
回転方法を [左右のみ v] にする
```

\--- /task \---

\--- task \---

ピンクのはしごを登るには、上向き矢印がを押され**かつ**キャラクターが正しい色に触れている時にいつも、キャラクタースプライトは数歩ステージの上方へ移動します。

`もし` {:class="block3control"} `上向きの矢印が押され` {:class="block3sensing"}そして、キャラクタが`ピンクに触れている`{:class="block3sensing"}場合に、 キャラクターの`ずっと` {:class="block3control"}ループの内側に追加し、キャラクターの`y`位置 (縦方向)を`変えます` {:class="block3motion"}

![ピコウォーキングスプライト](images/pico_walking_sprite.png)

```blocks3
    もし <<key (up arrow v) pressed?> かつ <touching color [#FF69B4]?>> なら 
  y座標を (4) ずつ変える
end
```

\--- /task \---

\--- task \---

コードをテストしましょう。 キャラクターをピンクのはしごに登らせて、レベルの最後まで到達させることができますか？

![スクリーンショット](images/dodge-test-character.png)

\--- /task \---