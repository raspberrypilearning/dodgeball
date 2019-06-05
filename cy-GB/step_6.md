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
pan fo'r flag werdd yn cael ei glicio
cuddio
am byth 
  aros (3) eiliad
  creu clôn o (myself v)
end
```

```blocks3
pan rwy'n dechrau fel clôn
mynd i x: (160) y: (160)
dangos
ailadrodd (22) 
  newid y gan (-4)
end
ailadrodd (170) 
  newid x gan (-2)
  troi (6) gradd i'r chwith
end
ailadrodd (30) 
  newid y gan (-4)
end
dileu y clôn hw
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
ailadrodd (170) 
  newid x gan (-2)
  troi (6) gradd i'r chwith
end

ailadrodd (180) 
  newid x gan (2)
  troi (6) gradd i'r dde
end

ailadrodd (30) 
  newid y gan (-4)
end
```

\--- /hint \---

\--- hint \---

Fe ddylai'r cloniau pêl edrych fel hyn:

![corlun pêl](images/ball_sprite.png)

```blocks3
pan rwy'n dechrau fel clôn
mynd i x: (160) y: (160)
dangos
ailadrodd (22) 
  newid y gan (-4)
end
ailadrodd (170) 
  newid x gan (-2)
  troi (6) gradd i'r chwith
end
ailadrodd (30) 
  newid y gan (-4)
end
ailadrodd (180) 
  newid x gan (2)
  troi (6) gradd i'r dde
end
ailadrodd (30) 
  newid y gan (-4)
end
ailadrodd (170) 
  newid x gan (-2)
  troi (6) gradd i'r chwith
end
dileu y clôn hwn
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Nawr ychwanega blociau côd i ddarlledu (Anfon) neges os yw dy gymeriad yn cael ei daro gan bêl!

Ychwanega'r côd yma i'r corlun pêl:

![corlun pêl](images/ball_sprite.png)

```blocks3
    pan rwy'n dechrau fel clôn
am byth 
  os yna
  darlledu (hit v)
end > then
darlledu (hit v)
end
end
```

\--- /task \---

\--- task \---

Yn olaf, ychwanega flociau côd i'r cymeriad fel ei fod yn symud yn ôl i'r man cychwyn pan mae'n derbyn y neges `taro`:

![corlun cerdded pico](images/pico_walking_sprite.png)

```blocks3
    pan rwy'n derbyn [hit v]
pwyntio i gyfeiriad (90)
mynd i x: (-210) y: (-120
```

\--- /task \---

\--- task \---

Profa dy gôd. Gwiria os yw'r cymeriad yn symud yn ôl i'r cychwyn ar ôl cyffwrdd y bêl.

\--- /task \---