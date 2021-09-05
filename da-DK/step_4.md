## Tyngdekraft og at hoppe

Nu skal du få din figur til at bevæge sig mere realistisk: du kommer til at tilføje tyngdekraft til dit spil, og give figuren evnen til at hoppe.

--- task ---

Bevæg din figur i spillet så den træder ud over kanten af en platform. Kan du se at den kan gå på luften?

![screenshot](images/dodge-no-gravity.png)

--- /task ---

--- task ---

For at fikse dette, skal du tilføje tyngdekraft til dit spil. Du gør dette ved at lave en ny variabel kaldt `gravity`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Hvis du foretrækker det, kan du skjule denne variabel fra dit niveau.

![screenshot](images/dodge-gravity-annotated.png)

--- /task ---

--- task ---

Tilføj disse nye kodeblokke som sætter `gravity` til et negativt tal og bruger værdien af `gravity` til at ændre din figurs y-koordinat konstant:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	when flag clicked
	set [gravity v] to [-4]
	forever
		change y by (gravity)
	end
```

--- /task ---

--- task ---

Tryk på flaget, og derefter træk din figur til toppen af niveauet. Hvad sker der? Opfører tyngdekraften sig som forventet?

![screenshot](images/dodge-gravity-drag.png)

--- /task ---

--- task ---

Tyngdekraft burde ikke flytte figur spriten igennem en platform eller en stige! Tilføj en `if`{:class="block3control"} blok til din kode som gør, at tyngdekraften kun virker, når figuren er i luften. Tyngdekraftskoden bør nu se således ud:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	when flag clicked
	set [gravity v] to [-4]
	forever
		if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
			change y by (gravity)
		end
	end
```

--- /task ---

--- task ---

Test spillet igen for at se om tyngdekraften virker rigtigt nu. Stopper din figur sprite med at falde, når den rører en platform eller en stige? Kan du få figuren til at træde ud over kanten af en platform og falde ned til platformen nedenunder?

![screenshot](images/dodge-gravity-test.png)

--- /task ---

--- task ---

Du skal du tilføje kode der får din figur til at hoppe, når spilleren trykker på <kbd>mellemrumstasten</kbd>. En meget let måde at gøre dette er at flytte din figur op et par gange:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	when [space v] key pressed
	repeat (10)
		change y by (4)
	end
```

Eftersom tyngdekraften hele tiden skubber din figur ned med 4 pixels, er du nødt til at vælge et tal større end `4` i din `change y by (4)`{:class="block3motion"} blok. Ændre tallet indtil du er tilfreds med den højde, din figur hopper.

--- /task ---

--- task ---

Test din kode. Bemærk at overgangen fra hop til fald er ret pludselig. For at få det til at være mere glidende, er du nødt til at få din figur til at bevæge sig mindre og mindre, indtil den ikke stiger længere.

--- /task ---

--- task ---

For at gøre dette, skal du lave en ny variabel kaldt `jump height`{:class="block3variables"}. Ligesom med `gravity` kan du skjule denne variabel, hvis du foretrækker det.

--- /task ---

--- task ---

Slet hoppekoden du tilføjede til din figur sprite, og tilføj denne kode i stedet for:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	when [space v] key pressed
	set [jump height v] to [8]
	repeat until < (jump height) = [0] >
		change y by (jump height)
		change [jump height v] by (-0.5)
	end
```

Denne kode flytter din figur op, først med 8 pixels, og derefter 7.5 pixels, 7 pixels, og så videre, indtil den ikke længere flytter op. Dette får hoppebevægelsen til at se bedre ud.

--- /task ---

--- task ---

Ændre værdien af `jump height`{:class="block3variables"} variablen, som er sat før `repeat`{:class="block3control"} starter. Test derefter dit spil.

Gentag disse to trin, indtil du er tilfreds med den højde, din figur hopper.

--- /task ---
