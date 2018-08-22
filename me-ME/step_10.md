--- challenge ---

## Izazov: Poboljšana gravitacija

Postoji još jedna mala greška u tvojoj igri: gravitacija ne vuče karaktera nadolje ako on *bilo kojim* svojim dijelom dodiruje plavu platformu - pa čak i svojom glavom! To možeš da isprobaš tako što ćeš se popeti skoro do vrha ljestvi, a zatim krenuti ulijevo.

![screenshot](images/dodge-gravity-bug.png)

Možeš li da ispraviš ovu grešku? Da to uradiš, potrebno je da svom karakteru promijeniš boju pantalona (u *svim* kostimima)...

![screenshot](images/dodge-trousers.png)

... a zatim zamijeniš kôd:

```blocks
    < touching color [#0000FF]? >
```

sa:

```blocks
    < color [#00FF00] is touching [#0000FF]? >
```

Ne zaboravi da isprobaš svoja poboljšanja i provjeriš da li je greška ispravljena!

--- /challenge ---