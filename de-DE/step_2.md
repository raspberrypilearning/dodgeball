## Bewegung der Spielfigur

Erstelle als Erstes einen Charakter, der sich nach links und rechts bewegen und auf Leitern klettern kann.

\--- task \---

Öffne das Scratch-Startprojekt 'Dodgeball'.

**Online:** Öffne das Basisprojekt auf [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){:target="_blank"}.

Wenn du bereits einen Scratch-Account besitzt, kannst du dir durch Klick auf **Remix** eine Kopie anlegen.

**Offline:** Lade das Basisprojekt von [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get){:target="_blank"} herunter und öffne es dann mit dem Scratch Offline-Editor.

\--- /task \---

Das Projekt enthält einen Hintergrund mit Plattformen:

![dodgeball project background](images/dodge-background.png)

\--- /task \---

Wähle ein neues Sprite als Charakter, den der Spieler steuern wird, und füge es zu deinem Projekt hinzu. Es ist am besten, wenn du ein Sprit mit mehreren Kostümen wählst, damit du es so aussehen lässt, als ob es geht.

![pick a sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- /task \---

Füge Code-Blöcke zu deinem Zeichen Sprite hinzu, damit der Spieler die Pfeiltasten verwenden kann, um den Charakter umher zu bewegen. Wenn der Spieler den Rechtspfeil drückt, sollte der Charakter nach rechts zeigen, ein paar Schritte gehen und zum nächsten Kostüm wechseln:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
when flag clicked
forever
    if <key (right arrow v) pressed? > then
        point in direction (90 v)
        move (3) steps
        next costume
    end
end
```

\--- /task \---

\--- /task \---

Wenn dein Sprite nicht passt, passe die Größe an.

![set sprite size so it fits](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- /task \---

Teste die Figur deines Spielers, indem du auf die Flagge klickst und dann den Pfeil nach oben gedrückt hältst. Bewegt sich dein Charakter nach rechts? Sieht dein Charakter so aus, als würde er laufen?

![screenshot](images/dodge-walking.png)

\--- /task \---

\--- /task \---

Füge Code-Blöcke zu den Zeichensprite `forever`{:class="block3control"} Schleife hinzu, so dass es links geht, wenn die linke Pfeiltaste gedrückt wird.

\--- /task \---

\--- /task \---

Damit sich dein Charakter nach links bewegen kann, musst du einen weiteren `if`{:class="block3control"} Block in der `forever`{:class ="block3control"} (fortlaufend wiederholend) Schleife hinzufügen. In diesen neuen ` if ` {: class = "block3control"} Block, füge einen Code hinzu, um deinen Sprite Charakter nach links zu `zu bewegen` {: class = "block3motion"}.

\--- /task \---

\--- /task \---

Kopiere den Code, den du erstellt hast, um den Charakter nach rechts laufen zu lassen. Stelle dann die gedrückte Taste `key pressed` {: class = "block3sensing"} auf Links-Pfeil`left arrow` {: class = "block3sensing"}, und ändere die Richtung `direction` {: class = "block3motion"} auf `-90`.

```blocks3
if <key (right arrow v) pressed? > then
    point in direction (90 v)
    move (3) steps
    next costume
end
```

\--- /task \---

\--- /task \---

Dein Code sollte so aussehen:

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

\--- /task \---

Teste den neuen Code, um sicherzustellen, dass er funktioniert. Stellt sich dein Charakter auf den Kopf, wenn du nach links gehst?

![screenshot](images/dodge-upside-down.png)

Wenn ja, kannst du dies beheben, indem du auf die Richtung **direction** von deinen Charakter Sprite klickst und dann auf den Pfeil nach links und rechts klickst.

![screenshot](images/dodge-left-right-annotated.png)

Wenn du möchtest, kannst du das Problem auch beheben, indem du diesen Block am Anfang des Skripts deines Charakters einfügst:

```blocks3
set rotation style [left-right v]
```

\--- /task \---

\--- /task \---

Um eine rosafarbene Leiter zu besteigen, sollte sich dein Charakter-Sprite auf dem Spielfeld ein paar Schritte nach oben bewegen, wenn der Aufwärtspfeil gedrückt wird **und ** der Charakter die richtige Farbe berührt.

Füge zu der fortlaufend wiederholend `forever`{:class="block3control"} Schleife deines Charakters, um die ` y ` (vertikale) Position des Charakters zu verändern ` change ` {: class = "block3motion"}, wenn `if` {: class = "block3control"} der Aufwärtspfeil gedrückt ist `up arrow is pressed`{:class="block3sensing"} und der Charakter die pinke Farbe' berührt `touching the colour pink`{:class="block3sensing"}, hinzu.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

\--- /task \---

\--- /task \---

Teste deinen Code. Schaffst du es, dass der Charakter die rosafarbenen Leitern erklimmt und das Ende des Levels erreicht?

![screenshot](images/dodge-test-character.png)

\--- /task \---