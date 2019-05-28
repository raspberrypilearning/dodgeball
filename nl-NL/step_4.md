## Zwaartekracht en springen

Je gaat nu jouw personage realistischer laten bewegen: je gaat zwaartekracht aan je spel toevoegen en het personage de mogelijkheid geven om te springen.

\--- task \----

Verplaats in het spel je personage zodat het van een platform afloopt. Zie je dat het in de lege ruimte kan lopen?

![screenshot](images/dodge-no-gravity.png)

\--- /task \---

\--- task \----

Om dit te verhelpen, voegen we zwaartekracht toe aan je spel. Maak hiervoor een nieuwe variabele met de naam `zwaartekracht`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Je kunt deze variabele verbergen als je dat wilt.

![screenshot](images/dodge-gravity-annotated.png)

\--- /task \---

\--- task \---

Voeg deze nieuwe codeblokken toe die de `zwaartekracht` instelt op een negatief getal en daarna de waarde `zwaartekracht` gebruikt om de y-coördinaat van je personage herhaaldelijk te veranderen:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    wanneer groene vlag wordt aangeklikt
maak [zwaartekracht v] [-4]
herhaal 
  verander y met (zwaartekracht)
end
```

\--- /task \---

\--- task \---

Klik op de vlag en sleep het personage naar de bovenkant van het werkgebied. Wat gebeurt er? Werkt de zwaartekracht zoals je had verwacht?

![screenshot](images/dodge-gravity-drag.png)

\--- /task \---

\--- task \----

Zwaartekracht zou je personage niet door een platform of een ladder moeten laten gaan! Voeg een `als`{:class="block3control"} -blok toe aan je code zodat de zwaartekracht alleen werkt wanneer je personage in de lucht is. De zwaartekrachtcode zou er nu als volgt uit moeten zien:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    wanneer groene vlag wordt aangeklikt
maak [zwaartekracht v] [-4]
herhaal 
  als <niet <<raak ik kleur [#003fff] ?> of <raak ik kleur [#ff00bf] ?>>> dan 
    verander y met (zwaartekracht)
  end
end
```

\--- /task \---

\--- task \----

Test het spel opnieuw om te zien of de zwaartekracht nu correct werkt. Stopt je personage met vallen wanneer het een platform of een ladder raakt? Kun je het personage van de rand van de platforms laten lopen en op het onderliggende niveau laten vallen?

![screenshot](images/dodge-gravity-test.png)

\--- /task \---

\--- task \---

Voeg nu code toe om er voor te zorgen dat je personage springt wanneer de speler op de <kbd>spatiebalk</kbd> drukt. Een heel eenvoudige manier om dit te doen is je personage een paar keer omhoog te bewegen:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    wanneer [spatiebalk v] wordt ingedrukt
herhaal (10) keer 
  verander y met (4)
end
```

Omdat de zwaartekracht je personage steeds met 4 pixels omlaag duwt, moet je een getal groter dan `4` kiezen in het blok `verander y met (4)`{:class="block3motion"}. Wijzig het nummer totdat je tevreden bent met de hoogte die het personage springt.

\--- /task \---

\--- task \---

Test je code. Merk op dat de sprongbeweging niet erg soepel verloopt. Om het springen soepeler te laten lijken, moet je het personage in steeds kleinere stapjes verplaatsen, totdat het niet meer springt.

\--- /task \---

\--- task \----

Maak hiervoor een andere variabele met de naam `springhoogte`{:class="block3variables"} aan. Je kunt deze variabele weer verbergen als je dat wilt.

\--- /task \---

\--- task \---

Verwijder de springcode die je aan je personage hebt toegevoegd en vervang die door deze code:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    wanneer [spatiebalk v] wordt ingedrukt
maak [springhoogte v] [8]
herhaal tot <(springhoogte) = [0]> 
  verander y met (springhoogte)
  verander [springhoogte v] met (-0.5)
end
```

Deze code verplaatst je personage omhoog, eerst met 8 pixels, dan met 7,5 pixels, dan 7 pixels, enzovoorts, totdat het personage klaar is met springen. Hierdoor ziet springen er veel soepeler uit.

\--- /task \---

\--- task \----

Wijzig de waarde van de `springhoogte`{:class="block3variables"} variabele die vóór de `herhaal`{:class="block3control"}-lus is ingesteld. Test je spel.

Herhaal deze twee stappen totdat je tevreden bent met hoe hoog het personage springt.

\--- /task \---