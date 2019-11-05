## Schwerkraft und springen

Jetzt bringstdue deinen Charakter dazu, sich realistischer zu bewegen: Du wirst deinem Spiel Schwerkraft verleihen und dem Charakter die Möglichkeit zum Springen geben.

\--- task \---

Im Spiel bewegt sich dein Charakter, als ob er von einer Plattform geht. Siehst du, dass er in leeren Raum gehen kann?

![screenshot](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

Um dies zu beheben, füge dem Spiel Schwerkraft hinzu. Erstelle eine neue Variable namens Schwerkraft `gravity`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Du kannst diese Variable aus deinem Spielfeld ausblenden, wenn du möchtest.

![Screenshot](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Füge diese neuen Codeblöcke hinzu, um die `gravity` auf eine negative Zahl festzulegen und verwende den Wert von `gravity`, um die y-Koordinate deines Charakters fortlaufend zu ändern:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        change y by (gravity)
    end
```

\--- /task \---

\--- task \---

Klicke auf die Flagge und ziehe deinen Charakter an den oberen Rand des Spielfeldes. Was ist passiert? Funktioniert die Schwerkraft wie erwartet?

![Screenshot](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Die Schwerkraft sollte das Sprite des Charakters nicht über eine Plattform oder eine Leiter bewegen! Füge einen `if`{:class="block3control"} Baustein zu deinen Code hinzu, um die Schwerkraft nur dann funktionieren zu lassen, wenn das Zeichen in der Mitte ist. Der Schwerkraftcode sollte dann so aussehen:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravity v] to [-4]
    forever
        if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
            change y by (gravity)
        end
    end
```

\--- /task \---

\--- task \---

Teste das Spiel erneut, um zu sehen, ob die Schwerkraft jetzt korrekt funktioniert. Fällt dein Charakter-Sprit nicht mehr, wenn er eine Plattform oder eine Leiter berührt? Kannst du den Charakter dazu bringen, von den Rändern der Plattformen zu laufen und auf das Level darunter zu fallen?

![Screenshot](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Füge nun einen Code hinzu, um deinen Charakter springen zu lassen, wenn der Spieler die Leertaste<kbd>space</kbd> drückt. Eine sehr einfache Möglichkeit, dies zu tun, besteht darin, deinen Charakter ein paar Mal nach oben zu bewegen:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    repeat (10)
        change y by (4)
    end
```

Da die Schwerkraft Ihren Charakter ständig 4 Pixel nach unten drückt, musst du eine Zahl größer als `4 ` wählen in deinen `change y by (4)`{:class="block3motion"} Block. Ändere die Zahl, bis du mit der Höhe, in der der Charakter springt, zufrieden bist.

\--- /task \---

\--- task \---

Teste deinen Code. Beachte, dass die Sprungbewegung nicht sehr flüssig ist. Damit das Springen flüssiger aussieht, musst du deinen Sprite Charakter immer in kleiner und kleiner werdende Mengen bewegen, bis es nicht mehr höher steigt.

\--- /task \---

\--- task \---

Hierzu erstelle eine neue Variable namens Sprunghöhe `jump height`{:class="block3variables"}. Auch diese Variable kannst du ausblenden, wenn du möchtest.

\--- /task \---

\--- task \---

Lösche den Sprungcode, den du deinem Zeichensprite hinzugefügt hast, und füge stattdessen diesen Code hinzu:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    set [jump height v] to [8]
    repeat until < (jump height) = [0] >
        change y by (jump height)
        change [jump height v] by (-0.5)
    end
```

Dieser Code verschiebt deinen Charakter um 8 Pixel, dann um 7,5 Pixel, dann um 7 Pixel usw., bis er nicht mehr höher steigt. Das macht das Springen viel geschmeidiger.

\--- /task \---

\--- task \---

Ändere den Wert der Sprunghöhe `jump height` {: class = "block3variables"} Variablen, welche vor dem Starten der Wiederholung `repeat` {: class = "block3control"} gesetzt wird. Teste nun dein Spiel.

Wiederhole diese beiden Schritte, bis du mit der Höhe des springenden Charakters zufrieden bist.

\--- /task \---