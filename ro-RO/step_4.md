## Gravitate si sarituri

Acum vei face ca personajul tău să se miște mai realist: vei adăuga gravitatea jocului tău și îi vei da abilității să sară.

\--- proba\---

În joc, mișcați personajul astfel încât să plece de pe o platformă. Vedeți că poate merge în spațiu gol?

![captură de ecran](images/dodge-no-gravity.png)

\--- /task \---

\--- proba\---

Pentru a rezolva aceasta, adăugați gravitate jocului tău. Pentru aceasta, creați o nouă variabilă numită `gravitație`{: class = "block3variables"}.

[[[generic-scratch3-add-variable]]]

Puteți să ascundeți această variabilă din Stadiul dvs. dacă doriți.

![captură de ecran](images/dodge-gravity-annotated.png)

\--- /task \---

\--- proba\---

Adăugați aceste blocuri noi de cod care stabilesc `gravitație` la un număr negativ și utilizați valoarea `gravitație` pentru a modifica în mod repetat coordonatele y ale personajului dvs.:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravitate v] to [-4]
    forever
        change y by (gravitate)
    end
```

\--- /task \---

\--- proba\---

Faceți clic pe pavilion, apoi glisați caracterul dvs. în partea de sus a scenei. Ce se itampla? Acționează gravitatea așa cum vă așteptați?

![captură de ecran](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Gravitatea nu ar trebui să miște caracterul sprite printr-o platformă sau o scară! Adăugați o blocare `dacă blocul`{: class = "block3control"} la codul dvs. pentru a lăsa lucrarea gravitațională doar atunci când personajul se află în mijlocul aerului. Codul de gravitate ar trebui să arate astfel:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
    when flag clicked
    set [gravitate v] to [-4]
    forever
        if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
            change y by (gravitate)
        end
    end
```

\--- /task \---

\--- proba\---

Testați din nou jocul pentru a vedea dacă gravitatea funcționează corect acum. Caracterul dvs. sprite nu se încadrează atunci când atinge o platformă sau o scară? Poti face ca personajul sa mearga de pe marginea platformelor si sa cada pe nivelul de mai jos?

![captură de ecran](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Acum adaugati codul pentru a face saltul personajului de fiecare data cand jucatorul apasa tasta <kbd>spatiu</kbd>. O modalitate foarte ușoară de a face acest lucru este să vă mișcați personajul de câteva ori:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    repeat (10)
        change y by (4)
    end
```

Deoarece gravitația îți împinge caracterul în mod constant cu 4 pixeli, trebuie să alegi un număr mai mare de `4` în blocul tău de `modificări y (4)`{: class = "block3motion"}. Modificați numărul până când sunteți mulțumit de înălțimea pe care personajul o sărută.

\--- /task \---

\--- proba\---

Testați-vă codul. Observați că mișcarea de sărituri nu este foarte netedă. Pentru a face săriturile să arate mai bine, trebuie să vă mișcați sprite de caractere cu cantități mai mici și mai mici, până când nu crește nici mai mult.

\--- /task \---

\--- proba\---

Pentru aceasta, creați o nouă variabilă denumită `înălțime de salt`{: class = "block3variables"}. Din nou, puteți ascunde această variabilă dacă preferați.

\--- /task \---

\--- task \---

Ștergeți codul de jumping pe care l-ați adăugat la caracterul dvs. sprite și adăugați în schimb acest cod:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
    when [space v] key pressed
    set [inaltime salt v] to [8]
    repeat until < (inaltime salt) = [0] >
        change y by (inaltime salt)
        change [inaltime salt v] by (-0.5)
    end
```

Acest cod mișcă caracterul dvs. cu până la 8 pixeli, apoi cu 7,5 pixeli, apoi cu 7 pixeli și așa mai departe, până când nu crește nici mai mult. Acest lucru face ca sariturile sa arate mult mai real.

\--- /task \---

\--- task \---

Modificați valoarea variabilei `înălțime de salt`{: class = "block3variables"} care este setată înainte de începerea celei de-a `repetări`{: class = "block3control"}. Atunci testați-vă jocul.

Repetați acești doi pași până când sunteți mulțumiți de cât de mare este caracterul.

\--- /task \---