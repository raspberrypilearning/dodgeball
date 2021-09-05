## Figur bevægelse

Start med at lave en figur, som kan bevæge sig til venstre og til højre, og som kan klatre op af stiger.

--- task ---

Åben 'Dodgeball' Scratch starterprojektet.

**Online:** åben starterprojektet ved [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){:target="_blank"}. 

Hvis du har en Scratch konto, kan du lave en kopi ved at klikke **Remix**.

**Offline:** download starterprojektet fra [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get) og åben det derefter med offline redigeringsprogrammet.

--- /task ---

Projektet indeholder en baggrund med platforme:

![dodgeball projekt baggrund](images/dodge-background.png)

--- task ---

Vælg en ny sprite som den figur, spilleren vil styre, og tilføj det til dit projekt. Det vil være bedst hvis du vælger en sprite med flere stillinger (kaldt kostumer - 'costumes' - i Scratch), så du kan få figuren til at se ud som om, at den går rundt.

![vælg en sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Tilføj kodeblokke til din figur sprite, så spilleren kan bruge piletasterne til at bevæge figuren. Når spilleren trykker den højre pil, bør figuren pege til højre, bevæge sig nogle få skridt, og skifte til det næste kostume:

![pico bevægelses sprite](images/pico_walking_sprite.png)

```blocks3
when flag clicked
forever
	if <key (right arrow v) pressed? > then
		point in direction (90 v)
		move (3) steps
		next costume
	end
end
```

--- /task ---

--- task ---

Hvis din sprite ikke passer, så juster dets størrelse.

![sæt sprite størrelse så det passer](images/dodge-sprite-size-annotated.png)

--- /task ---

--- task ---

Test din figur ved at klikke på flaget og derefter trykke på den højre piletast. Bevæger din figur til højre? Ligner det, at figuren går rundt?

![screenshot](images/dodge-walking.png)

--- /task ---

--- task ---

Tilføj kodeblokke til `forever`{:class="block3control"} loopet af figurens sprite, så den vil gå til venstre, når der trykkes på venstre pil.

--- hints ---

--- hint ---

For at få din figur til at gå til venstre, er du nødt til at tilføje en ny `if`{:class="block3control"} blok inde i `forever`{:class="block3control"} loopet. I denne nye `if`{:class="block3control"} blok, skal du tilføje kode for at få figurens sprite til at gå til venstre med `move`{:class="block3motion"}.

--- /hint ---

--- hint ---

Kopier den kode du skrev til at få figuren til at gå til højre. Sæt derefter `key pressed`{:class="block3sensing"} til `left arrow`{:class="block3sensing"}, og skift `direction`{:class="block3motion"} til `-90`.

```blocks3
if <key (right arrow v) pressed? > then
	point in direction (90 v)
	move (3) steps
	next costume
end
```

--- /hint ---

--- hint ---

Din kode burde se sådan her ud:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
when green flag clicked
forever 
  if <key (right arrow v) pressed?> then 
    point in direction (90 v)
    move (3) steps
    next costume
  end
  if <key (left arrow v) pressed?> then 
    point in direction (-90 v)
    move (3) steps
    next costume
  end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Test din nye kode for at sikre, at det virker. Vender din figur på hovedet, når den går til venstre?

![screenshot](images/dodge-upside-down.png)

Hvis dette sker, kan du fikse det ved at klikke på **direction** elementet af din figur, og derefter klikke på venstre-højre pilen.

![screenshot](images/dodge-left-right-annotated.png)

Hvis du foretrækker det, kan du i stedet fikse problemet ved at tilføje denne blok til starten af din figurs script:

```blocks3
set rotation style [left-right v]
```

--- /task ---

--- task ---

For at klatre en lyserød stige bør din figur sprite bevæge nogle trin opad på banen, når op pilen er trykket **og** figuren rører den rette farve.

Tilføj følgende kode til din figur's `forever`{:class="block3control"} loop for at ændre - `change`{:class="block3motion"} - figurens `y` (lodrette) position hvis - `if`{:class="block3control"} - op pilen er trykket - `up arrow is pressed`{:class="block3sensing"} - og figuren rører farven lyserød - `touching the colour pink`{:class="block3sensing"}.

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
		change y by (4)
	end
```

--- /task ---

--- task ---

Test din kode. Kan du få figuren til at klatre de lyserøde stiger og nå slutningen af levelet?

![screenshot](images/dodge-test-character.png)

--- /task ---
