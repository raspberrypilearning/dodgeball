\--- challenge \---

## Provocare: Imbunatatirea controlului gravitatii

Există încă o mică greșeală în joc: gravitatia nu vă trage în jos personajul dacă *any* o parte atinge o platformă albastră - chiar și capul! Puteți testa acest lucru urcând mai sus pe o scară și apoi mutând spre stânga.

![captură de ecran](images/dodge-gravity-bug.png)

Puteti rezolva acest neajuns? Pentru a face acest lucru, trebuie sa dai personajului tau diferite culori pantalonilor (on *all* costumes)...

![captură de ecran](images/dodge-trousers.png)

... și apoi înlocuiți liniile de cod:

```blocks
    < touching color [#0000FF]? >
```

cu: 

```blocks
    < color [#00FF00] is touching [#0000FF]? >
```

Nu uitați să vă testați îmbunătățirile pentru a vă asigura că ați rezolvat problema!

\--- /challenge \---