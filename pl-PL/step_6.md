## Unikanie piłek

Twoja postać może się teraz poruszać i skakać, więc czas dodać kilka piłek, których postać musi unikać.

--- task ---

Utwórz nowego duszka piłkę. Możesz wybrać dowolny typ piłki który chcesz.

![zrzut ekranu](images/dodge-balls.png)

--- /task ---

--- task ---

Zmień rozmiar piłki, tak by Twoja postać mogła ją przeskoczyć. Postaraj się, aby postać przeskoczyła nad piłką, aby sprawdzić, czy piłka ma odpowiedni rozmiar.

![zrzut ekranu](images/dodge-ball-resize.png)

--- /task ---

--- task ---

Dodaj poniższy kod do duszka piłki:

![duszek piłki](images/ball_sprite.png)

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

--- /task ---

--- task ---

Kliknij flagę, aby przetestować grę.

![zrzut ekranu](images/dodge-ball-test.png)

--- /task ---

--- task ---

Dodaj więcej kodu do swojego duszka piłki, aby jej klony poruszały się po wszystkich trzech platformach.

![zrzut ekranu](images/dodge-ball-more-motion.png)

--- hints ---

--- hint ---

Powtórz bloki kodu, których użyłaś, aby przesuwać klon duszka piłki po pierwszej platformie. Musisz zmienić liczby `x`{:class="block3motion"}, `y`{:class="block3motion"} i `powtarzaj`{:class="block3control"} liczby, aby klony poprawnie podążały za platformami.

--- /hint ---

--- hint ---

Oto bloki, których potrzebujesz. Upewnij się, że dodałaś je we właściwej kolejności.

![duszek piłki](images/ball_sprite.png)

```blocks3
powtarzaj (170) 
  zmień x o (-2)
  obróć ccw o (6) stopni
koniec

powtarzaj (180) 
  zmień x o (2)
  obróć cw o (6) stopni
koniec

powtarzaj (30) 
  zmień y o (-4)
koniec
```

--- /hint ---

--- hint ---

Kod twoich klonów duszka piłki powinien wyglądać następująco:

![duszek piłki](images/ball_sprite.png)

```blocks3
gdy zaczynam jako klon
idź do x: (160) y: (160)
pokaż
powtórz (22) 
  zmień y o (-4)
koniec
powtarzaj (170) 
  zmień x o (-2)
  obróć ccw o (6) stopni
koniec
powtarzaj (30) 
  zmień y o (-4)
koniec
powtarzaj (180) 
  zmień x o (2)
  obróć cw o (6) stopni
koniec
powtarzaj (30) 
  zmień y o (-4)
koniec
powtarzaj (170) 
  zmień x o (-2)
  obróć ccw o (6) stopni
koniec
usuń tego klona
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Teraz dodaj kilka bloków kodu, aby nadawać (wysłać) wiadomość, jeśli twoja postać zostanie trafiona piłką!

Dodaj poniższy kod do duszka piłki:

![duszek piłki](images/ball_sprite.png)

```blocks3
    gdy zaczynam jako klon
    zawsze
        jeżeli < dotyka (Pico walking v)? > to
            nadaj komunikat (trafienie v)
        koniec
    koniec
```

--- /task ---

--- task ---

Na koniec dodaj bloki kodu do duszka postaci, aby powrócił do swojej pozycji początkowej kiedy dostaje komunikat `trafienie`:

![duszek Pico walking](images/pico_walking_sprite.png)

```blocks3
    kiedy otrzymam [trafienie v]
    ustaw kierunek na (90)
    idź do x: (-210) y: (-120)
```

--- /task ---

--- task ---

Przetestuj swój kod. Sprawdź, czy po dotknięciu piłki postać wraca na początek.

--- /task ---