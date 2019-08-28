## Poruszanie się postacią

Zacznij od stworzenia postaci która może poruszać się w lewo i w prawo oraz wspinać się po drabinach.

\--- task \---

Otwórz projekt startowy Scratch „Dwa ognie”.

**Online:** otwórz nowy projekt Scratcha na stronie [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){:target="_blank"}.

Jeśli masz konto Scratch, możesz wykonać kopię klikając **Remiks**.

**Offline:** pobierz projekt początkowy z [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get), i otwórz w programie Scratch Desktop.

\--- /task \---

Projekt zawiera tło z platformami:

![dodgeball project background](images/dodge-background.png)

\--- task \---

Wybierz nowego duszka jako postać, którą gracz będzie kontrolować i dodaj go do swojego projektu. Będzie najlepiej, jeśli wybierzesz duszka z wieloma kostiumami, wtedy będziesz mógł sprawić, że będzie wyglądać jakby chodził.

![pick a sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Dodaj bloki kodu do duszka postaci, aby gracz mógł używać klawiszy strzałek do poruszania się postacią. Gdy gracz naciśnie prawą strzałkę, Twoja postać powinna ustawić się w prawo, poruszyć się kilka kroków i zmienić kostium na następny:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
kiedy flaga kliknięta
zawsze
    jeżeli <klawisz (strzałka w prawo v) naciśnięty? > to
        ustaw kierunek na (90 v)
        przesuń o (3) kroki
        następny kostium
    koniec
koniec
```

\--- /task \---

\--- task \---

Jeśli Twój duszek nie pasuje, dostosuj jego rozmiar.

![set sprite size so it fits](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Przetestuj Twoją postać, klikając na flagę i przytrzymując klawisz prawej strzałki. Czy Twoja postać porusza się w prawo? Czy Twoja postać wygląda jakby się poruszała?

![screenshot](images/dodge-walking.png)

\--- /task \---

\--- task \---

Dodaj bloki kodu do pętli `zawsze`{:class="block3control"} duszka postaci, w taki sposób, żeby postać poruszała się w lewo po naciśnięciu klawisza lewej strzałki.

\--- hints \---

\--- hint \---

Aby Twoja postać mogła poruszyć się w lewo, będziesz musiała dodać kolejny blok `jeżeli`{:class="block3control"} wewnątrz pętli `zawsze`{:class="block3control"}. W tym nowym bloku `jeżeli`{:class="block3control"}, dodaj kod, aby twój duszek postaci `poruszył się`{:class="block3motion"} w lewo.

\--- /hint \---

\--- hint \---

Skopiuj utworzony kod, aby spowodować, żeby postać poszła w prawo. Następnie ustaw w bloku `klawisz naciśnięty`{:class="block3sensing"} `strzałka w lewo`{:class="block3sensing"} i zmień `kierunek`{:class="block3motion"} na `-90`.

```blocks3
if <key (right arrow v) pressed? > then
    point in direction (90 v)
    move (3) steps
    next costume
end
```

\--- /hint \---

\--- hint \---

Your code should look like this now:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
when green flag clicked
forever 
  if <key (right arrow v) pressed?> then 
    point in direction (90 v)
    move (3) steps
    next costume
  end
  if <key (left arrow v) pressed?> then 
    point in direction (-90 v)
    move (3) steps
    next costume
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Test your new code to make sure that it works. Does your character turn upside-down when walking to the left?

![screenshot](images/dodge-upside-down.png)

If so, you can fix this by clicking on the **direction** of your character sprite, and then clicking on the left-right arrow.

![screenshot](images/dodge-left-right-annotated.png)

Or if you prefer, you can also fix the problem by adding this block to the start of your character's script:

```blocks3
ustaw styl obrotu [lewo-prawo v]
```

\--- /task \---

\--- task \---

To climb a pink ladder, your character sprite should move a few steps upwards on the Stage whenever the up arrow is pressed **and** the character is touching the correct colour.

Add inside your character's `forever`{:class="block3control"} loop to `change`{:class="block3motion"} the character's `y` (vertical) position `if`{:class="block3control"} the `up arrow is pressed`{:class="block3sensing"} and the character is `touching the colour pink`{:class="block3sensing"}.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    jeżeli <<key (up arrow v) pressed?> i <touching color [#FF69B4]?> > to
        zmień y o (4)
    end
```

\--- /task \---

\--- task \---

Test your code. Can you make the character climb the pink ladders and get to the end of the level?

![screenshot](images/dodge-test-character.png)

\--- /task \---