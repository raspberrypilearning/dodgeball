## Udfordring: forbedret tyngdekraft

Der er en anden, lille bug i dit spil: tyngdekraften hiver ikke figur spriten ned, så længe at __en hvilken som helst__ del af spriten rører en blå platform. Så selv hvis spritens hoved rører en platform, vil spriten ikke falde! Du kan teste dette: få din figur til at klatre op det meste af en stige, og derefter flyt figuren til siden under en platform:

![screenshot](images/dodge-gravity-bug.png)

For at fikse bug'en, skal du først give din figur sprite nye bukser, som har en anderledes farve (på __alle__ kostumer).

![screenshot](images/dodge-trousers.png)

Derefter erstatter du denne kodeblok:

```blocks3
	< touching color [#0000FF]? >
```

Med denne kodeblok:

```blocks3
	< color [#00FF00] is touching [#0000FF]? >
```

Test spillet efter du har lavet disse ændringer, for at sikre at du har fikset bug'en!
