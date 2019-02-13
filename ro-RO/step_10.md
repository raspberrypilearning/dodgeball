## Provocare: îmbunătățirea gravitației

Există încă un bug mic în joc: gravitatea nu trage caracterul sprite în jos dacă **orice** parte a sprite atinge o platformă albastră. Deci, chiar dacă capul sprites atinge o platformă, sprite nu cădea! Puteți încerca singuri acest lucru: faceți ca personajul să urce mai mult pe o scară și apoi mutați caracterul lateral sub o platformă:

![captură de ecran](images/dodge-gravity-bug.png)

Pentru a rezolva bug - ul, trebuie mai întâi pentru a da sprite personaj pantaloni noi , care au o culoare diferită (pe **toate** costume).

![captură de ecran](images/dodge-trousers.png)

Apoi înlocuiți acest bloc de cod:

```blocks3
    < touching color [#0000FF]? >
```

cu acest bloc de cod:

```blocks3
    < color [#00FF00] is touching [#0000FF]? >
```

Pentru a vă asigura că ați rezolvat problema, încercați jocul după ce ați făcut aceste modificări!