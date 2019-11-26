## Herausforderung: Verbesserte Schwerkraft

Es gibt einen anderen kleinen Fehler in deinem Spiel: die Schwerkraft zieht den Charakter nicht nach unten, wenn **irgendein** Teil des Charakters eine blaue Plattform berührt. Selbst wenn der Kopf des Charakters eine Plattform berührt, fällt der Charakter nicht! Du kannst dies selbst testen: Lass deinen Charakter weit auf einer Leiter hinauf klettern und bewege dann deinen Charakter unter eine Plattform:

![Screenshot](images/dodge-gravity-bug.png)

Um den Fehler zu beheben, musst du zuerst deinem Charakter neue Hosen mit einer anderen Farbe geben (auf **allen** Kostümen).

![Screenshot](images/dodge-trousers.png)

Ersetze diesen Code-Block:

```blocks3
    < wird Farbe [#0000FF] berührt? >
```

mit diesem Codeblock:

```blocks3
    < Farbe [#00FF00] berührt [#0000FF]? >
```

Um sicherzustellen, dass du den Fehler behoben hast, teste das Spiel, nachdem du diese Änderungen vorgenommen hast!