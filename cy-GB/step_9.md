## Her: mwy o rwystrau

Os wyt ti dal i feddwl bod dy gêm yn rhy hawdd, mae modd i ti ychwanegu mwy o rwystrau. Mae modd i ti ychwanegu unrhywbeth! Dyma rai syniadau:

+ Pili-pala sy’n hedfan
+ Platfform sydd yn ymddangos a diflannu
+ Peli tenis sydd yn rhaid osgoi

![sgrinlun](images/dodge-obstacles.png)

Mae modd i ti hefyd greu cefndir arall i greu lefel arall. Yna ychwanega gôd, fel pan fo'r cymeriad yn cyrraedd y drws gwyrdd, mae'r gêm yn newid i'r cefndir newydd:

![corlun cerdded pico](images/pico_walking_sprite.png)

```blocks3
    os <cyffwrdd lliw [#00FF00] ?> yna 
  newid cefndir i (cefnlen nesaf v)
  mynd i x: (-210) y: (-120)
  aros (1) eiliad
end
```