## Evita mingea

Personajul tău se poate mișca și să sară acum, deci e timpul să adaugi niște bile pe care personajul trebuie să le evite.

\--- proba\---

Creați un nou model de minge. Puteți alege orice tip de minge care vă place.

![captură de ecran](images/dodge-balls.png)

\--- /proba\---

\--- task \---

Redimensionați sprite-ul, astfel încât personajul să poată sări peste el. Încercați să faceți saltul de caracter peste minge pentru a testa dacă mingea are dimensiunea potrivită.

![captură de ecran](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Adăugați aceste linii de cod la modelul dvs. de minge:

![mingea sprite](images/ball_sprite.png)

```blocks3
când steagul verde a dat clic
ascunde
pentru totdeauna 
  așteptați (3) secunde
  creați clona de (eu v)
sfârșit
```

```blocks3
când încep ca o clona
du - te la x: (160) y: (160)
arată
repeat (22) 
  schimbarea y de (-4)
final
repeat (170) 
  schimbare x prin (-2)
  rândul său, ccw (6) grade
final
repetați (30) 
  schimbați y cu (-4)
sfârșitul
ștergeți această clonă
```

Acest cod creează o nouă clonă a sprite-ului cu bile la fiecare trei secunde. Fiecare clonă nouă se deplasează de-a lungul platformei de vârf și apoi scade.

\--- /task \---

\--- proba\---

Faceți clic pe steag pentru a testa jocul.

![captură de ecran](images/dodge-ball-test.png)

\--- /task \---

\--- proba\---

Adăugați mai mult cod la sprite-ul dvs. de minge, astfel încât clonele acestuia să se deplaseze pe toate cele trei platforme.

![captură de ecran](images/dodge-ball-more-motion.png)

\--- sugestii \---

\--- indiciu \---

Repetați blocurile de cod pe care le-ați folosit pentru a muta clona sprite mingea pe prima platformă. Trebuie să modificați numerele `x`{class = "block3motion"}, `y`{: class = "block3motion"} și `repetiții`{: class = "block3control"} astfel încât clonele să urmeze corect platformele .

\--- / indiciu \---

\--- indiciu \---

Acestea sunt blocurile de care aveți nevoie. Asigurați-vă că le adăugați în ordinea corectă.

![mingea sprite](images/ball_sprite.png)

```blocks3
repeat (170) 
  schimbare x prin (-2)
  ccw rândul său (6) grade
end

repeat (180) 
  schimbare x prin (2)
  cw rândul său (6) grade
end

repeat (30) 
  schimbarea y de către (-4)
capăt
```

\--- / indiciu \---

\--- hint \---

Codul pentru clonele sprite de bile ar trebui să arate astfel:

![mingea sprite](images/ball_sprite.png)

```blocks3
când încep ca o clona
du - te la x: (160) y: (160)
arată
repeat (22) 
  schimbarea y de (-4)
final
repeat (170) 
  schimbare x prin (-2)
  rândul său , ccw (6) grade
capăt
repeat (30) 
  schimbarea y de (-4)
final
repeat (180) 
  schimbare x prin (2)
  cw rândul său (6) grade
extremitate
repeat (30) 
  schimbare y prin (-4)
sfârșitul
repet (170) 
  schimbare x prin (-2)
  răsfoire ccw (6) grade
sfârșitul
ștergeți această clonă
```

\--- / indiciu \---

\--- / sugestii \---

\--- /task \---

\--- proba\---

Acum adăugați niște blocuri de coduri pentru a transmite (trimite) un mesaj dacă personajul tău este lovit de o minge!

Adăugați aceste linii de cod la modelul dvs. de minge:

![mingea sprite](images/ball_sprite.png)

```blocks3
    când încep ca o clonă
    pentru totdeauna
        dacă < atinge (Pico m)? > atunci
            difuzat (lovit v)
        sfârșitul
    sfârșit
```

\--- /task \---

\--- proba\---

În cele din urmă, adăugați blocuri de coduri pentru caracterul dvs. sprite, pentru al face să se mute înapoi la poziția sa inițială atunci când primește mesajul `hit`:

![pictori de mers pe jos pico](images/pico_walking_sprite.png)

```blocks3
    când primesc [hit v]
    punct în direcție (90)
    mergi la x: (-210) y: (-120)
```

\--- /task \---

\--- proba\---

Testați-vă codul. Verificați dacă personajul se mută înapoi la început după atingerea unei mingi.

\--- /task \---