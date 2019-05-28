## Osgoi peli

Nawr fod dy gymeriad yn symud o gwmpas, fe awn ati i ychwanegu peli bydd yn rhaid i dy gymeriad osgoi.

\--- task \---

Mae angen creu corlun pêl newydd. Fe alli di ddewis unrhyw fath o bêl yr hoffet ti.

![sgrinlun](images/dodge-balls.png)

\--- /task \---

\--- task \---

Newida maint dy bêl fel bod dy gymeriad yn medru neidio drosto. Ceisia neidio dros y bêl i’w brofi ei fod y maint cywir.

![sgrinlun](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Ychwanega'r côd yma i'r corlun pêl:

![corlun pêl](images/ball_sprite.png)

```blocks3
when green flag clicked
hide
forever 
  wait (3) seconds
  create clone of (myself v)
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

Mae’r côd yma yn creu pêl newydd bob 3 eiliad. Mae pob pêl newydd yn symud ar draws top y platfform yna yn disgyn.

\--- /task \---

\--- task \---

Clicia ar y faner i brofi'r gêm.

![sgrinlun](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Ychwanega mwy o gôd i giplun dy bêl, fel eu bod yn symud ar draws y 3 platfform.

![sgrinlun](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Ail-adrodda'r blociau côd wnes di eu defnyddio i symud clôn y bêl ar draws y platfform cyntaf. Bydd angen i ti newid `x`{:class="block3motion"}, `y`{:class="block3motion"}, ac `ail-adrodd`{:class="block3control"} y rhifau fel bod y cloniau yn dilyn y platfform yn union.

\--- /hint \---

\--- hint \---

Dyma'r blociau côd rwyt ti eu hangen. Gwna'n siŵr dy fod yn eu hychwanegu yn y drefn gywir.

![corlun pêl](images/ball_sprite.png)

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

\--- /hint \---

\--- hint \---

Fe ddylai'r cloniau pêl edrych fel hyn:

![corlun pêl](images/ball_sprite.png)

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

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Nawr ychwanega blociau côd i ddarlledu (Anfon) neges os yw dy gymeriad yn cael ei daro gan bêl!

Ychwanega'r côd yma i'r corlun pêl:

![corlun pêl](images/ball_sprite.png)

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

Yn olaf, ychwanega flociau côd i'r cymeriad fel ei fod yn symud yn ôl i'r man cychwyn pan mae'n derbyn y neges `taro`:

![corlun cerdded pico](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Profa dy gôd. Gwiria os yw'r cymeriad yn symud yn ôl i'r cychwyn ar ôl cyffwrdd y bêl.

\--- /task \---