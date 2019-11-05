## Springende Bälle

Dein Charakter kann sich jetzt bewegen und springen, also ist es Zeit, ein paar Bälle hinzuzufügen, die der Charakter meiden muss.

\--- task \---

Erstelle ein neues Kugel-Sprite. Du kannst jede Art von Ball nehmen, die du möchtest.

![screenshot](images/dodge-balls.png)

\--- /task \---

\--- task \---

Ändere die Größe des Ball-Sprites, damit der Charakter darüber springen kann. Versuche den Charakter über den Ball springen zu lassen, um zu testen, ob der Ball die richtige Größe hat.

![Screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Füge diesen Code deinem Ballsprite hinzu:

![ball sprite](images/ball_sprite.png)

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

Dieser Code erstellt alle drei Sekunden einen neuen Klon des Ball-Sprites. Jeder neue Klon bewegt sich auf der obersten Plattform und fällt dann.

\--- /task \---

\--- task \---

Klicke auf die Flagge, um das Spiel zu testen.

![Screenshot](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Füge deinem Kugelsprit mehr Codes hinzu, damit Klone von ihm sich über alle drei Plattformen hinweg bewegen.

![Screenshot](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Wiederhole die Codeblöcke, mit denen du den Ball-Sprite-Klon über die erste Plattform bewegt hast. Du musst die `x`{:class="block3motion"}, `y`{:class="block3motion"}, und `repeat`{:class="block3control"} Zahlen ändern, damit die Klone den Plattformen korrekt folgen.

\--- /hint \---

\--- hint \---

Hier sind die Codeblöcke die du brauchst. Stelle sicher, dass du sie in der richtigen Reihenfolge hinzufügst.

![ball sprite](images/ball_sprite.png)

```blocks3
epeat (170) 
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

Der Code für deine Kugelsprite Klone sollte wie folgt aussehen:

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

\--- /hint \---

\---/hints\---

\--- /task \---

\--- task \---

Füge nun einige Code-Blöcke hinzu, um eine Nachricht zu übertragen (senden), wenn dein Charakter von einem Ball getroffen wird!

Füge diesen Code deinem Ballsprite hinzu:

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

Füge schließlich Code-Blöcke zu deinem Zeichensprite hinzu, um es zu seiner Startposition zurückzuziehen, wenn es die Treffer `hit` Nachricht erhält:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Teste deinen Code. Überprüfe, ob der Charakter nach dem Berühren eines Balls zum Start zurückkehrt.

\--- /task \---