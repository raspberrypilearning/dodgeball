## Cinematica personajului

Începeți prin a crea un personaj care se poate deplasa spre stânga și spre dreapta și poate urca pe scări.

\--- proba\---

Deschideți proiectul Starter Scratch "Dodgeball".

**Online:** deschideți proiectul starter la [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){: target = "_ blank"}.

**Offline:** descărcați proiectul de pornire de la [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get) și apoi deschideți-l folosind editorul offline.

\--- /task \---

Proiectul conține un fundal cu platforme:

![fundul proiectului dodgeball](images/dodge-background.png)

\--- task \---

Alegeți un nou sprite ca personajul pe care playerul îl va controla și adăugați-l în proiect. Cel mai bine este să alegeți un sprite cu mai multe costume, astfel încât să puteți face să pară ca și cum ar merge.

![alege un sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Adăugați blocuri de coduri pentru personajul dvs. sprite astfel încât playerul să poată utiliza tastele săgeți pentru a muta caracterul în jur. Când jucătorul apasă săgeata dreapta, caracterul trebuie să fie îndreptat spre dreapta, să meargă câțiva pași și să se schimbe costumul următor:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
când steagul a dat clic
pentru totdeauna
    dacă tasta <(săgeata la dreapta v) a fost apăsată? > apoi
        punct în direcție (90 v)
        mișcare (3) trepte
        costum următor
    capăt
capăt
```

\--- /task \---

\--- proba\---

Dacă sprite dvs. nu se încadrează, ajustați dimensiunea sa.

![setați mărimea sprite astfel încât să se potrivească](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Testați caracterul dvs. făcând clic pe steag și apoi ținând apăsată tasta săgeată dreapta. Personajul tău se mișcă spre dreapta? Caracterul tău arată ca și cum merge?

![captură de ecran](images/dodge-walking.png)

\--- /task \---

\--- task \---

Adăugați blocuri de coduri pentru buclă de caracter `forțată`{: class = "block3control"} astfel încât să meargă la stânga dacă apăsați tasta săgeată stânga.

\--- sugestii \---

\--- indiciu \---

Pentru ca caracterul dvs. să se poată deplasa spre stânga, va trebui să adăugați o altă blocare `cazul blocului`{: class = "block3control"} în interiorul celei de-a `buclă`{: class = "block3control"}. În acest nou bloc `dacă blocul`{: class = "block3control"}, adăugați un cod pentru a crea caracterul dvs. sprite `mutați`{: class = "block3motion"} în stânga.

\--- / indiciu \---

\--- hint \---

Copiați codul pe care l-ați creat pentru a face caracterul să meargă spre dreapta. Apoi setați `apăsată tasta`{: class = "block3sensing"} la `la stânga săgeată`{: class = "block3sensing"} și schimbați `direcția`{: class = "block3motion"} la `-90`.

```blocks3
dacă apăsați tasta <(săgeata dreapta v)? > apoi
    punct în direcție (90 v)
    mișcare (3) trepte
    costum următor
capăt
```

\--- / indiciu \---

\--- hint \---

Codul dvs. ar trebui să arate astfel:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
când steagul verde apasat
pentru totdeauna 
  dacă <key (right arrow v) pressed?> , apoi 
    punct în direcția (90 v)
    mutare (3) pașii
    costum următor
  capăt
  dacă <key (left arrow v) pressed?> atunci 
    punct în direcția (-90 v)
    mutare (3) pașii
    next costum
  sfârșitul
sfârșitul
```

\--- / indiciu \---

\--- / sugestii \---

\--- /task \---

\--- proba\---

Testați noul cod pentru a vă asigura că funcționează. Personajul tău se răstoarnă când merge la stânga?

![captură de ecran](images/dodge-upside-down.png)

Dacă da, puteți rezolva acest lucru făcând clic pe **direcția** din sprite tău caracter, apoi făcând clic pe săgeata stânga-dreapta.

![captură de ecran](images/dodge-left-right-annotated.png)

Sau, dacă preferați, puteți remedia problema adăugând acest bloc la începutul scriptului personajului dvs.:

```blocks3
setati modul de rotatie [left-right v]
```

\--- /task \---

\--- proba\---

Pentru a urca pe o scară roz, personajul dvs. sprite trebuie să se miște cu câțiva pași în sus pe scenă ori de câte ori săgeata în sus este apăsată **și** caracterul atinge culoarea corectă.

Adăugați în interiorul personajului tău `totdeauna`{: class = "block3control"} bucla la `schimbare`{: class = "block3motion"} personajului `y` (verticală) `dacă este`{: class = "block3control"} `săgeata în sus este apăsată`{: class = "block3sensing"}} iar caracterul este de `atinge culoarea roz`{: class = "block3sensing"}.

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

\--- /task \---

\--- task \---

Testați-vă codul. Poți face ca personajul să urce scările roz și să ajungă la sfârșitul nivelului?

![captură de ecran](images/dodge-test-character.png)

\--- /task \---