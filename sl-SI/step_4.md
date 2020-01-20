## Gravitacija in skoki

Sedaj poskrbi, da se bo tvoj lik premikal bolj realistično: igri dodaj gravitacijo in liku omogoči, da lahko skače.

\--- task \---

V igri pojdi s svojim likom tako daleč, da bo šel preko ploščadi. Kot vidiš lahko hodi po praznem prostoru.

![posnetek zaslona](images/dodge-no-gravity.png)

\--- /task \---

\--- task \---

Popravi to tako, da igri dodaš gravitacijo. V ta namen ustvari novo spremenljivko imenovano `gravitacija`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

To spremenljivko lahko po želji skriješ, da se ne vidi na odru.

![posnetek zaslona](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Dodaj nove bloke kode, ki nastavijo `gravitacijo` na negativno vrednost in uporabi vrednost `gravitacije`, da ponavljaš spremembo y-položaja lika:

![piko hodeča figura](images/pico_walking_sprite.png)

```blocks3
    ko kliknemo na zastavo
  nastavi [gravitacija v] na [-4]
  ponavljaj
    spremni y za (gravitacija)
  konec
```

\--- /task \---

\--- task \---

Klikni na zastavo in povleci svoj lik na vrh odra. Kaj se zgodi? Ali gravitacija deluje po pričakovanju?

![posnetek zaslona](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \---

Gravitacija ne bi smela premakniti figure lika skozi ploščad ali lestev! Dodaj blok `če`{:class="block3control"}, ki bo omogočal delovanje gravitacije le ladar je lik v zraku. Koda gravitacija naj bo videti tako:

![piko hodeča figura](images/pico_walking_sprite.png)

```blocks3
    ko kliknemo na zastavo
  nastavi [gravitacija v] na [-4]
  ponavljaj
    če < ne <<se dotika barve [#0000FF]?> ali <se dotika barve [#FF69B4]?>>> potem
      spremni y za (gravitacija)
    konec
  konec
```

\--- /task \---

\--- task \---

Ponovno preizkusi igro, da vidiš, če sedaj gravitacija deluje pravilno. Ali tvoja tvoja figura lika preneha padati, ko se dotakne ploščadi ali lestve? Lahko narediš, da lik pade en nivo nižje, kadar gre preko roba ploščadi?

![posnetek zaslona](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Sedaj dodaj kodo, ki bo poskrbela, da bo tvoj lik skočil, kadar bo igralec pritisnil tipko <kbd>presledek</kbd>. Enostaven način za to je, da svoj lik nekajkrat pomakneš navzgor:

![piko hodeča figura](images/pico_walking_sprite.png)

```blocks3
    ko je pritisnjena tipka [presledek v]
  ponovi (10) krat
    spremeni y za (4)
  konec
```

Ker gravitacija neprestano sili lik za 4 piksle navzdol, moraš izbrati številko, ki je večja od `4` v bloku `spremeni y za (4)`{:class="block3motion"}. Spreminjaj številko, dokler ti višina skoka ne ustreza.

\--- /task \---

\--- task \---

Preizkusi svojo kodo. Premikanje med skokom ni preveč mehko. Da bi skok bil videti bolj mehak, je potrebno tvoj lik premikati za vedno manjše korake, dokler se sploh več ne dviguje.

\--- /task \---

\--- task \---

V ta namen ustvari novo spremenljivko `višina skoka`{:class="block3variables"}. Če hočeš, lahko tudi to spremenljivko skriješ.

\--- /task \---

\--- task \---

Izbriši kodo za skok, ki si jo dodal figuri lika in namesto nje dodaj to kodo:

![piko hodeča figura](images/pico_walking_sprite.png)

```blocks3
    ko je pritisnjena tipka [presledke v]
  nastavi [višina skoka v] na [8]
  ponavljaj do < (višina skoka) = [0] >
    spremeni y za (višina skoka)
    spremeni [višina skoka v] za (-0.5)
  konec
```

Ta koda premakne tvoj lik za 8 pikslov navzgor, nato za 7,5 pikslov, nato za 7 pikslov in tako dalje, dokler se več ne dviguje. Tako bo skok videti veliko bolj mehak.

\--- /task \---

\--- task \---

Spremeni vrednost spremenljivke `višina skoka`{:class="block3variables"}, ki se nastavi preden se izvede zanka `ponavljaj do`{:class="block3control"}. Nato preizkusi svojo igro.

Ponovi ta dva koraka, dokler ti višina skoka ne ustreza.

\--- /task \---