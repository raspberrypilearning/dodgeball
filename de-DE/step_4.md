## Schwerkraft und springen

Jetzt bringst du deinen Charakter dazu, sich realistischer zu bewegen: Du wirst deinem Spiel Schwerkraft verleihen und dem Charakter die Möglichkeit zum Springen geben.

--- task ---

Im Spiel bewegt sich dein Charakter, als ob er von einer Plattform geht. Siehst du, dass er in leeren Raum gehen kann?

![Screenshot](images/dodge-no-gravity.png)

--- /task ---

--- task ---

Um dies zu beheben, füge dem Spiel Schwerkraft hinzu. Erstelle eine neue Variable namens `Schwerkraft`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Du kannst diese Variable aus deinem Spielfeld ausblenden, wenn du möchtest.

![Screenshot](images/dodge-gravity-annotated.png)

--- /task ---

--- task ---

Füge diese neuen Codeblöcke hinzu, um die `Schwerkraft` auf eine negative Zahl festzulegen und verwende den Wert von `Schwerkraft`, um die y-Koordinate deines Charakters fortlaufend zu ändern:

![Pico-Walking Sprite](images/pico_walking_sprite.png)

```blocks3
when flag clicked
set [Schwerkraft v] to [-4]
forever 
  change y by (Schwerkraft)
end
```

--- /task ---

--- task ---

Klicke auf die Flagge und ziehe deinen Charakter an den oberen Rand des Spielfeldes. Was ist passiert? Funktioniert die Schwerkraft wie erwartet?

![Screenshot](images/dodge-gravity-drag.png)

--- /task ---

--- task ---

Die Schwerkraft sollte das Sprite des Charakters nicht durch eine Plattform oder eine Leiter bewegen! Füge einen `falls`{:class="block3control"} Baustein zu deinen Code hinzu, um die Schwerkraft nur dann funktionieren zu lassen, wenn das Zeichen in der Mitte ist. Der Schwerkraftcode sollte dann so aussehen:

![Pico-Walking Sprite](images/pico_walking_sprite.png)

```blocks3
when flag clicked
set [Schwerkraft v] to [-4]
forever 
  if <not <<touching color [#0000FF] ?> or <touching color [#FF69B4] ?>>> then 
    change y by (Schwerkraft)
  end
end
```

--- /task ---

--- task ---

Teste das Spiel erneut, um zu sehen, ob die Schwerkraft jetzt korrekt funktioniert. Fällt dein Charakter-Sprit nicht mehr, wenn er eine Plattform oder eine Leiter berührt? Kannst du den Charakter dazu bringen, von den Rändern der Plattformen zu laufen und auf das Level darunter zu fallen?

![Screenshot](images/dodge-gravity-test.png)

--- /task ---

--- task ---

Füge nun einen Code hinzu, um deinen Charakter springen zu lassen, wenn der Spieler die <kbd>Leertaste</kbd> drückt. Eine sehr einfache Möglichkeit, dies zu tun, besteht darin, deinen Charakter ein paar Mal nach oben zu bewegen:

![Pico-Walking Sprite](images/pico_walking_sprite.png)

```blocks3
when [Leertaste v] key pressed
repeat (10) 
  change y by (4)
end
```

Da die Schwerkraft Ihren Charakter ständig 4 Pixel nach unten drückt, musst du eine Zahl größer als `4` wählen in deinen `ändere y um (4)`{:class="block3motion"} Block. Ändere die Zahl, bis du mit der Höhe, in der der Charakter springt, zufrieden bist.

--- /task ---

--- task ---

Teste deinen Code. Beachte, dass die Sprungbewegung nicht sehr flüssig ist. Damit das Springen flüssiger aussieht, musst du deinen Sprite Charakter immer in kleiner und kleiner werdende Mengen bewegen, bis es nicht mehr höher steigt.

--- /task ---

--- task ---

Hierzu erstelle eine neue Variable namens `Sprunghöhe`{:class="block3variables"}. Auch diese Variable kannst du ausblenden, wenn du möchtest.

--- /task ---

--- task ---

Lösche den Sprungcode, den du deinem Charakter-Sprite hinzugefügt hast, und füge stattdessen diesen Code hinzu:

![Pico-Walking Sprite](images/pico_walking_sprite.png)

```blocks3
when [Leertaste v] key pressed
set [Sprunghöhe v] to [8]
repeat until <(Sprunghöhe) = [0]> 
  change y by (Sprunghöhe)
  change [Sprunghöhe v] by (-0.5)
end
```

Dieser Code verschiebt deinen Charakter um 8 Pixel, dann um 7,5 Pixel, dann um 7 Pixel usw., bis er nicht mehr höher steigt. Das macht das Springen viel geschmeidiger.

--- /task ---

--- task ---

Ändere den Wert der `Sprunghöhe`{:class="block3variables"} Variable, welche vor dem Starten der Wiederholung `wiederhohle`{:class="block3control"} gesetzt wird. Teste nun dein Spiel.

Wiederhole diese beiden Schritte, bis du mit der Höhe des springenden Charakters zufrieden bist.

--- /task ---