## 挑戰：更多阻礙

如果你覺得遊戲太簡單，可以試著添加更多煩人的障礙物。 你喜歡什麼阻礙就給它加上去！ 給你一些好點子：

+ 四處亂飛的蝴蝶
+ 隨時消失的平台
+ 從天而降的網球

![截圖](images/dodge-obstacles.png)

你還可以設計下一個背景， 當角色抵達終點（綠色的方塊）後，切換到下一個背景，這樣一來你的遊戲就變成關卡式的遊戲了：

![正在走路的 Pico](images/pico_walking_sprite.png)

```blocks3
    if <touching color [#00FF00]?> then
		switch backdrop to (next backdrop v)
		go to x: (-210) y: (-120)
		wait (1) seconds
	end
```