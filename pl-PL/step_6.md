## Unikanie piłek

Twoja postać może się teraz poruszać i skakać, więc czas dodać kilka piłek, których postać musi unikać.

\--- task \---

Utwórz nowego duszka piłkę. Możesz wybrać dowolny typ piłki który chcesz.

![zrzut ekranu](images/dodge-balls.png)

\--- /task \---

\--- task \---

Zmień rozmiar piłki, tak by Twoja postać mogła ją przeskoczyć. Postaraj się, aby postać przeskoczyła nad piłką, aby sprawdzić, czy piłka ma odpowiedni rozmiar.

![zrzut ekranu](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Dodaj poniższy kod do duszka piłki:

![ball sprite](images/ball_sprite.png)

```blocks3
kiedy flaga kliknięta
ukryj
zawsze 
  czekaj (3) sekund
  utwórz klona z (siebie v)
koniec
```

```blocks3
gdy zaczynam jako klon
idź do x: (160) y: (160)
pokaż
powtarzaj (22) 
  zmień y o (-4)
koniec
powtarzaj (170) 
  zmień x o (-2)
  obróć ccw o (6) stopni
koniec
powtarzaj (30) 
  zmień y o (-4)
koniec
usuń tego klona
```

Ten kod tworzy nowy klon duszka piłki co trzy sekundy. Każdy nowy klon porusza się wzdłuż górnej platformy, a następnie spada.

\--- /task \---

\--- task \---

Kliknij flagę, aby przetestować grę.

![zrzut ekranu](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Dodaj więcej kodu do swojego duszka piłki, aby jej klony poruszały się po wszystkich trzech platformach.

![zrzut ekranu](images/dodge-ball-more-motion.png)

\--- wskazówka \---

\--- hint \---

Powtórz bloki kodu, których użyłaś, aby przesuwać klon duszka piłki po pierwszej platformie. Musisz zmienić `x`{:class="block3motion"}, `y`{:class="block3motion"} i `powtarzaj`{:class="block3control"} liczby, aby klony poprawnie podążały za platformami.

\--- /wskazówka \---

\--- hint \---

Oto bloki, których potrzebujesz. Upewnij się, że dodałaś je we właściwej kolejności.

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

\--- /wskazówka \---

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

\--- /wskazówka \---

\--- /wskazówka \---

\--- /task \---

\--- task \---

Now add some code blocks to broadcast (send) a message if your character gets hit by a ball!

Dodaj poniższy kod do duszka piłki:

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