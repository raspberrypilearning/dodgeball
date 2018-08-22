\--- challenge \---

## Provocare: Mai multe obstacole

Dacă credeți că jocul dvs. este încă prea ușor, puteți adăuga mai multe obstacole la nivelul dvs. Puteți adăuga orice doriți, dar iată câteva idei:

+ Un fluture ucigas;
+ Platforme care apar și dispar;
+ Mingii de tenis care cad si care trebuiesc evitate.

![captură de ecran](images/dodge-obstacles.png)

Ați putea crea chiar mai mult de un fundal și treceți la nivelul următor când caracterul dvs. ajunge la ușa verde:

```blocks
    if <touching color [#00FF00]?> then
        switch backdrop to [next backdrop v]
        go to x: (-210) y: (-120)
        wait (1) secs
    end
```

\--- /challenge \---