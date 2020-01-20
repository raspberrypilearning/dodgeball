## Izmikanje žogam

Tvoj lik se lahko zdaj premika in skače, zato je čas, da dodaš nekaj žog, ki se jim mora lik izogibati.

\--- task \---

Ustvari novo figuro žoge. Po želji lahko izbereš kakršnokoli žogo.

![posnetek zaslona](images/dodge-balls.png)

\--- /task \---

\--- task \---

Spremeni velikost žoge, tako da bo mogoče skočiti preko nje. Poskusi z likom skočiti preko žoge, da preizkusiš, ali je žoga prave velikosti.

![posnetek zaslona](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Svoji figuri žoge dodaj to kodo:

![figura žoge](images/ball_sprite.png)

```blocks3
ko kliknemo na zastavo
skrij
ponavljaj 
  počakaj (3) sekund
  ustvari dvojnika (myself v)
end
```

```blocks3
ko začnem kot dvojnik
pojdi na x: (160) y: (160)
pokaži
ponovi (22) krat 
  spremeni y za (-4)
end
ponovi (170) krat 
  spremeni x za (-2)
  obrni se za (6) stopinj v levo
end
ponovi (30) krat 
  spremeni y za (-4)
end
zbriši tega dvojnika
```

Ta koda ustvari dvojnika figure žoge na vsake tri sekunde. Vsak nov dvojnik se pojavi na vrhu ploščadi in potem pada.

\--- /task \---

\--- task \---

Klikni na zastavo, da preizkusiš igro.

![posnetek zaslona](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Dodaj še več kode svoji figuri, tako da se bodo njeni dvojniki premikali preko vseh treh ploščadi.

![posnetek zaslona](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Ponovi bloke kode, ki si jih uporabil za premikanje žoge preko prve ploščadi. Spremeniti moraš številke za `x`{:class="block3motion"}, `y`{:class="block3motion"}, in `ponovi`{:class="block3control"}, da bodo dvojniki pravilno sledili ploščadim.

\--- /hint \---

\--- hint \---

To so potrebni bloki. Poskrbi, da bodo dodani v pravilnem vrstnem redu.

![figura žoge](images/ball_sprite.png)

```blocks3
ponovi (170) krat 
  spremeni x za (-2)
  obrni se za (6) stopinj v levo
end

ponovi (180) krat 
  spremeni x za (2)
  obrni se za (6) stopinj v desno
end

ponovi (30) krat 
  spremeni y za (-4)
end
```

\--- /hint \---

\--- hint \---

Koda za dvojnike figure žoge mora izgledati tako:

![figura žoge](images/ball_sprite.png)

```blocks3
ko začnem kot dvojnik
pojdi na x: (160) y: (160)
pokaži
ponovi (22) krat 
  spremeni y za (-4)
end
ponovi (170) krat 
  spremeni x za (-2)
  obrni se za (6) stopinj v levo
end
ponovi (30) krat 
  spremeni y za (-4)
end
ponovi (180) krat 
  spremeni x za (2)
  obrni se za (6) stopinj v desno
end
ponovi (30) krat 
  spremeni y za (-4)
end
ponovi (170) krat 
  spremeni x za (-2)
  obrni se za (6) stopinj v levo
end
zbriši tega dvojnika
```

\--- /hint \---

\--- /namigi \---

\--- /task \---

\--- task \---

Zdaj dodaj kodo, ki bo objavila (poslala) sporočilo, kadar žoga zadane tvoj lik!

Figuri žoge dodaj to kodo:

![figura žoge](images/ball_sprite.png)

```blocks3
    ko začnem kot dvojnik
ponavljaj 
  če <se dotika (Pico walking v)>  potem 
    objavi (hit v)
  end
end
```

\--- /task \---

\--- task \---

Na koncu dodaj figuri lika še bloke kode, da se bo premaknila nazaj na začetni položaj, ko bo prejela sporočilo `zadet`:

![piko hodeča figura](images/pico_walking_sprite.png)

```blocks3
    ko prejmem [zadet v]
obrni se v smer (90)
pojdi na x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Preizkusi svojo kodo. Preveri, ali se lik premakne nazaj na začetek, potem ko se dotakne žoge.

\--- /task \---