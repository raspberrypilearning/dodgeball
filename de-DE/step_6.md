## Bällen ausweichen

Dein Charakter kann sich jetzt bewegen und springen, also ist es Zeit, ein paar Bälle hinzuzufügen, denen der Charakter auweichen muss.

\--- task \---

Erstelle eine neue Ball-Figur. Du kannst jede Art von Ball nehmen, die du möchtest.

![Screenshot](images/dodge-balls.png)

\--- /task \---

\--- task \---

Ändere die Größe der Ball-Figur, damit der Charakter darüber springen kann. Versuche den Charakter über den Ball springen zu lassen, um zu testen, ob der Ball die richtige Größe hat.

![Screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Füge diesen Code deiner Ball-Figur hinzu:

![Ball-Sprite](images/ball_sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
verstecke dich
wiederhole fortlaufend 
  warte (3) Sekunden
  erzeuge Klon von (mir selbst v)
end
```

```blocks3
Wenn ich als Klon entstehe
gehe zu x: (160) y: (160)
zeige dich
wiederhole (22) mal 
  ändere y um (-4)
end
wiederhole (170) mal 
  ändere x um (-2)
  drehe dich nach links um (6) Grad
end
wiederhole (30) mal 
  ändere y um (-4)
end
lösche diesen Klon
```

Dieser Code erstellt alle drei Sekunden einen neuen Klon der Ball-Figur. Jeder neue Klon bewegt sich auf der obersten Plattform und fällt dann.

\--- /task \---

\--- task \---

Klicke auf die Flagge, um das Spiel zu testen.

![Screenshot](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Füge deiner Ball-Figur mehr Code hinzu, damit Klone von ihr sich über alle drei Plattformen hinweg bewegen.

![Screenshot](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Wiederhole die Codeblöcke, mit denen du den Ball-Figur-Klon über die erste Plattform bewegt hast. Du musst die `x`{:class="block3motion"}, `y`{:class="block3motion"}, und `wiederhohle`{:class="block3control"} Zahlen ändern, damit die Klone den Plattformen korrekt folgen.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke die du brauchst. Stelle sicher, dass du sie in der richtigen Reihenfolge hinzufügst.

![Ball-Sprite](images/ball_sprite.png)

```blocks3
wiederhole (170) mal 
  ändere x um (-2)
  drehe dich nach links um (6) Grad
end

wiederhole (180) mal 
  ändere x um (2)
  drehe dich nach rechts um (6) Grad
end

wiederhole (30) mal 
  ändere y um (-4)
end
```

\--- /hint \---

\--- hint \---

Der Code für deine Ball-Figur Klone sollte wie folgt aussehen:

![Ball-Sprite](images/ball_sprite.png)

```blocks3
Wenn ich als Klon entstehe
gehe zu x: (160) y: (160)
zeige dich
wiederhole (22) mal 
  ändere y um (-4)
end
wiederhole (170) mal 
  ändere x um (-2)
  drehe dich nach links um (6) Grad
end
wiederhole (30) mal 
  ändere y um (-4)
end
wiederhole (180) mal 
  ändere x um (2)
  drehe dich nach rechts um (6) Grad
end
wiederhole (30) mal 
  ändere y um (-4)
end
wiederhole (170) mal 
  ändere x um (-2)
  drehe dich nach links um (6) Grad
end
lösche diesen Klon
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Füge nun einige Code-Blöcke hinzu, um eine Nachricht zu senden, wenn dein Charakter von einem Ball getroffen wird!

Füge diesen Code deiner Ball-Figur hinzu:

![Ball-Sprite](images/ball_sprite.png)

```blocks3
    Wenn ich als Klon entstehe
wiederhole fortlaufend 
  falls < wird (Pico walking v) berührt? > dann 
    sende (Treffer v) an alle
  end
end
```

\--- /task \---

\--- task \---

Füge schließlich Code-Blöcke zu deiner Charakter-Figur hinzu, um sie zu ihrer Startposition zurückzuziehen, wenn sie die `Treffer` Nachricht erhält:

![Pico-Walking Sprite](images/pico_walking_sprite.png)

```blocks3
    Wenn ich [Treffer v] empfange
setze Richtung auf (90) Grad
gehe zu x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Teste deinen Code. Überprüfe, ob der Charakter nach dem Berühren eines Balls zum Start zurückkehrt.

\--- /task \---