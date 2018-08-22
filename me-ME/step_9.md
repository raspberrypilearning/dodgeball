--- challenge ---

## Izazov: Više prepreka

Ako misliš da je tvoja igra još uvijek previše laka, nivou možeš da dodaš više prepreka. Možeš da dodaš šta god želiš, a evo nekoliko ideja:

+ Leteći leptir;
+ Platforme koje se pojavljuju i nestaju;
+ Teniske loptice koje padaju i koje treba izbjeći.

![screenshot](images/dodge-obstacles.png)

Možeš čak da kreiraš više pozadina i da pređeš na sljedeći nivo kada tvoj karakter stigne do zelenih vrata:

```blocks
    if <touching color [#00FF00]?> then
        switch backdrop to [next backdrop v]
        go to x: (-210) y: (-120)
        wait (1) secs
    end
```

--- /challenge ---