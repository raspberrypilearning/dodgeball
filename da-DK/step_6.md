## Undvige bolde

Din figur kan nu gå rundt og hoppe, så det er tid til at tilføje bolde, som figuren skal undvige.

--- task ---

Lav en ny bold sprite. Du kan frit vælge den type bold, du kan lide.

![screenshot](images/dodge-balls.png)

--- /task ---

--- task ---

Ændre boldens størrelse så figuren kan hoppe over den. Prøv at få figuren til at hoppe over bolden for at teste, om bolden har den rigtige størrelse.

![screenshot](images/dodge-ball-resize.png)

--- /task ---

--- task ---

Tilføj denne kode til din bold sprite:

![bold sprite](images/ball_sprite.png)

```blocks3
when green flag clicked
hide
forever 
  wait (3) seconds
  create clone of (myself v)
end
```

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
delete this clone
```

Denne kode laver en ny klon af bold spriten hvert tredje sekund. Hver klon bevæger sig langs den øverste platform og falder derefter ned.

--- /task ---

--- task ---

Klik på flaget for at teste spillet.

![screenshot](images/dodge-ball-test.png)

--- /task ---

--- task ---

Tilføj mere kode til din bold sprite så dets kloner bevæger sig langs alle tre platforme.

![screenshot](images/dodge-ball-more-motion.png)

--- hints ---

--- hint ---

Gentag kodeblokkene du brugte til at bevæge bold sprite klonen langs den første platform. Du er nødt til at ændre tallene for `x`{:class="block3motion"}, `y`{:class="block3motion"}, og `repeat`{:class="block3control"}, så klonerne følger platformene korrekt.

--- /hint ---

--- hint ---

Disse blokke er hvad du har brug for. Vær opmærksom på at tilføje dem i den rette rækkefølge.

![bold sprite](images/ball_sprite.png)

```blocks3
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end

repeat (180) 
  change x by (2)
  turn cw (6) degrees
end

repeat (30) 
  change y by (-4)
end
```

--- /hint ---

--- hint ---

Koden for dine bold sprite kloner bør se således ud:

![bold sprite](images/ball_sprite.png)

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (180) 
  change x by (2)
  turn cw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
delete this clone
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Tilføj nu nogle kodeblokke til at udsende en besked, hvis din figur bliver ramt af en bold! (`broadcast`{:class="block3control"})

Tilføj denne kode til din bold sprite:

![bold sprite](images/ball_sprite.png)

```blocks3
	when I start as a clone
	forever
		if < touching (Pico walking v)? > then
			broadcast (hit v)
		end
	end
```

--- /task ---

--- task ---

Tilføj til sidst kodeblokke til din figur sprite, der får den til at flytte tilbage til dens startposition, når den modtager `hit`-beskeden:

![pico gå sprite](images/pico_walking_sprite.png)

```blocks3
	when I receive [hit v]
	point in direction (90)
	go to x: (-210) y: (-120)
```	

--- /task ---

--- task ---

Test din kode. Undersøg, om figuren flytter tilbage til starten, når den rører en bold.

--- /task ---

