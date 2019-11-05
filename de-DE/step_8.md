## Laser!

Um dein Spiel ein wenig schwieriger beenden zu lassen, wirst du Laser hinzufügen!

\--- task \---

Füge ein neues Sprit zu deinem Spiel hinzu und nenne es `laser`. Es sollte zwei Kostüme haben: eins mit Ein 'on' und eins mit Aus 'off'.

![screenshot](images/dodge-lasers-costume1.png)

![Screenshot](images/dodge-lasers-costume1.png)

\--- /task \---

\--- task \---

Platziere dein neues Lasersprit zwischen zwei Plattformen.

![Screenshot](images/dodge-lasers-position.png)

\--- /task \---

\--- task \---

Füge diesen Code zu deinem Lasersprit hinzu, um ihn zwischen den beiden Kostümen wechseln zu lassen.

![laser sprite](images/laser_sprite.png)

```blocks3
    when flag clicked
    forever
        switch costume to (on v)
        wait (2) seconds
        switch costume to (off v)
        wait (2) seconds
    end
```

Wenn du möchtest, kannst du den oben gezeigten Code so ändern, dass das Sprite eine Zufalls `random` {: class = "block3operators"} Zeitspanne zwischen den Kostümwechseln wartet `waits` {: class = "block3control"}.

\--- /task \---

\--- task \---

Anschließend fügst du Code zu deinem Lasersprit hinzu, sodass der Lasersprit eine Treffer 'hit'-Nachricht sendet, wenn es den Charakter Sprite berührt.

\--- hints \---

\--- hint \---

Dieser Code sollte sehr ähnlich sein wie der Code, den du zu deinem Kugelsprite hinzugefügt hast.

\--- /hint \---

\--- hint \---

Kopier den Code, den du dem Ball-Objekt hinzufügst hast, um dieses Objekt Treffer zu senden `broadcast 'hit'` {: class = "block3control"}, wenn es deinen Charakter berührt `touching your character`{:class="block3sensing"}.

\--- /hint \---

\--- hint \---

Dies ist der Code, den du dafür hinzufügen sollst:

![laser sprite](images/laser_sprite.png)

```blocks3
when green flag clicked
forever 
  if <touching (Pico walking v) ?> then 
    broadcast (hit v)
  end
end
```

\--- /hint \---

\---/hints\---

Du musst keinen zusätzlichen Code zu deinem Charakterobjekt hinzufügen, da das Charakterobjekt bereits weiß, was es zu tun hat, wenn es Treffer senden`broadcast 'hit'`{:class="block3control"} erhält!

\--- /task \---

\--- task \---

Teste dein Spiel, um festzustellen, ob du den Charakter am Laser vorbeibewegen kannst. Wenn der Laser zu leicht oder zu schwer zu meiden ist, ändere die Wartezeit `wait` {: class = "block3control"} im Code für das Laserobjet.

\--- /task \---