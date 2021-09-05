## Lasere!

For at gøre dit spil en smule sværere at vinde, vil du nu tilføje lasere!

--- task ---

Tilføj en ny sprite til dit spil og kald det `laser`. Den bør have to kostumer: en kaldt 'on', og en kaldt 'off'.

![screenshot](images/dodge-lasers-costume1.png)

![screenshot](images/dodge-lasers-costume2.png)

--- /task ---

--- task ---

Placer din nye laser sprite mellem to platforme.

![screenshot](images/dodge-lasers-position.png)

--- /task ---

--- task ---

Tilføj kode til din laser sprite, der får den til at skifte mellem dens to kostumer.

![laser sprite](images/laser_sprite.png)

```blocks3
	when flag clicked
	forever
		switch costume to (on v)
		wait (2) seconds
		switch costume to (off v)
		wait (2) seconds
	end
```

Hvis du foretrækker det, kan du ændre koden vist ovenover, så spriten venter en tilfældig mængde tid mellem hver kostumeskift (her skal du bruge `wait`{:class="block3control"} og `random`{:class="block3operators"}).

--- /task ---

--- task ---

Tilføj til sidst kode til din laser sprite så den udsender en 'hit' besked, når den rører figur spriten.

--- hints ---

--- hint ---

Denne kode bør ligne den kode, du tilføjede til din bold sprite.

--- /hint ---

--- hint ---

Kopier den kode du tilføjede til bold spriten, så denne sprite udsender en 'hit' når den rører din figur (vigtist her er `broadcast`{:class="block3control"} og `touching`{:class="block3sensing"}).

--- /hint ---

--- hint ---

Dette er den kode du bør tilføje:

![laser sprite](images/laser_sprite.png)

```blocks3
when green flag clicked
forever 
  if <touching (Pico walking v) ?> then 
    broadcast (hit v)
  end
end
```

--- /hint ---

--- /hints ---

Du behøver ikke at tilføje ekstra kode til din figur sprite, eftersom den allerede ved hvad den skal gøre, når den modtager `broadcast 'hit'`{:class="block3control"}!

--- /task ---

--- task ---

Test dit spil for at se, om du kan flytte figuren forbi laseren. Hvis laseren er for let eller for svær at undgå, kan du ændre `wait`{:class="block3control"} tiderne i koden for laser spriten.

--- /task ---
