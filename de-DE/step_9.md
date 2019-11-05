## Herausforderung: Mehr Hindernisse

Wenn du denkst, dass dein Spiel noch zu einfach ist, kannst du mehr Hindernisse hierfür hinzufügen. Die Hindernisse können alles sein, was du willst! Hier sind ein paar Vorschläge:

+ Ein gefährlicher Schmetterling
+ Plattformen, die erscheinen und verschwinden
+ Fallende Tennisbälle, die vermieden werden müssen

![Screenshot](images/dodge-obstacles.png)

Du kannst sogar einen anderen Hintergrund entwerfen, um das nächste Level zu erstellen. Füge dann einen Code hinzu, sodass das Spiel in den neuen Hintergrund wechselt, wenn dein Charakter die grüne Tür erreicht:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if <touching color [#00FF00]?> then
        switch backdrop to (next backdrop v)
        go to x: (-210) y: (-120)
        wait (1) seconds
    end
```