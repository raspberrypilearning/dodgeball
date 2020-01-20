## Laser!

Pentru jocul dvs. un pic mai greu pentru a finaliza, aveți de gând să adăugați lasere!

\--- proba\---

Adăugați un nou sprite la joc și numiți-l `laser`. Ar trebui să aibă două costume: unul numit "pe" și unul numit "off".

![captură de ecran](images/dodge-lasers-costume1.png)

![captură de ecran](images/dodge-lasers-costume2.png)

\--- /task \---

\--- task \---

Plasați noul dvs. sprite laser între două platforme.

![captură de ecran](images/dodge-lasers-position.png)

\--- /task \---

\--- proba\---

Adăugați codul la sprite-ul laser pentru al face să treacă între cele două costume.

![laser sprite](images/laser_sprite.png)

```blocks3
    când pavilionul a dat clic
    pentru totdeauna
        costum pentru comutator pentru (pe v)
        așteptați (2) secunde
        costum de comutare la (oprit v)
        așteptați (2) secunde
    sfârșit
```

Dacă preferați, puteți schimba codul prezentat mai sus , astfel încât sprite `așteaptă`{: class = „block3control“} a `aleatoare`{: class = „block3operators“} cantitate de timp între schimbările costum.

\--- /task \---

\--- task \---

În cele din urmă, adăugați cod la sprite laser, astfel încât sprite laser transmite un mesaj "lovit" când atinge caracterul sprite.

\--- sugestii \---

\--- hint \---

Acest cod trebuie să fie foarte asemănător cu codul pe care l-ați adăugat la sprite-ul tău.

\--- / indiciu \---

\--- indiciu \---

Copiați codul pe care îl adăugați la sprite-ul pentru a face acest sprite `difuzat "lovit"`{: class = "block3control"} atunci când atinge `personajul tău`{: class = "block3sensing"}.

\--- / indiciu \---

\--- hint \---

Acesta este codul pe care trebuie să-l adăugați:

![laser sprite](images/laser_sprite.png)

```blocks3
când steagul verde a dat clic
pentru totdeauna 
  dacă <touching (Pico walking v) ?> apoi 
    difuzat (lovit v)
  sfârșitul sfârșitul

```

\--- / indiciu \---

\--- / sugestii \---

Nu aveți nevoie să adăugați niciun cod suplimentar caracterelor dvs. sprite, deoarece sprite-ul de caractere deja știe ce trebuie să facă atunci când primește mesajul de difuzare `'hit'`{: class = "block3control"}!

\--- /task \---

\--- task \---

Testați-vă jocul pentru a vedea dacă puteți mișca caracterul de lângă laser. Dacă laserul este prea ușor sau prea greu de evitat, schimba `asteptati`{: class = „block3control“} ori în codul pentru sprite cu laser.

\--- /task \---