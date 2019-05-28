## Trefballen

Je personage kan nu bewegen en springen, dus het is tijd om ballen toe te voegen die het personage moet ontwijken.

\--- task \----

Maak een nieuwe balsprite. Je kunt elke soort bal kiezen die je leuk vindt.

![screenshot](images/dodge-balls.png)

\--- /task \---

\--- task \---

Verklein de balsprite zodat het personage eroverheen kan springen. Probeer het personage over de bal te laten springen om te testen of de bal de juiste maat heeft.

![screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \----

Voeg deze code toe aan je balsprite:

![balsprite](images/ball_sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
verdwijn
herhaal 
  wacht (3) seconden
  maak kloon van (ikzelf v)
end
```

```blocks3
wanneer ik als kloon start
ga naar x: (160) y: (160)
verschijn
herhaal (22) 
  verander y met (-4)
end
herhaal (170) 
  verander x met (-2)
  draai tegen de klok in (6) graden
end
herhaal (30) 
  verander y met (-4)
end
verwijder deze kloon
```

Deze code maakt om de drie seconden een nieuwe kloon van de balsprite. Elke nieuwe kloon rolt over het bovenste platform en valt vervolgens naar beneden.

\--- /task \---

\--- task \----

Klik op de vlag om het spel te testen.

![screenshot](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Voeg meer code toe aan je balsprite, zodat klonen ervan over alle drie platforms bewegen.

![screenshot](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Herhaal de codeblokken die je hebt gebruikt om de balsprite kloon over het eerste platform te bewegen. Je moet de `x` {:class="block3motion"}, `y`{:class="block3motion"}, en het aantal keren dat de `herhaal`{:class="block3control"} moet worden uitgevoerd wijzigen zodat de klonen de platforms correct volgen.

\--- /hint \---

\--- hint \---

Dit zijn de blokken die je nodig hebt. Zorg ervoor dat je ze in de juiste volgorde toevoegt.

![balsprite](images/ball_sprite.png)

```blocks3
herhaal (170) 
  verander x met (-2)
  draai tegen de klok in (6) graden
end

herhaal (180) 
  verander x met (2)
  draai met de klok mee (6) graden
end

herhaal (30) 
  verander y met (-4)
end
```

\--- /hint \---

\--- hint \---

De code voor jouw bal sprite klonen zou er zo moeten uitzien:

![bal sprite](images/ball_sprite.png)

```blocks3
wanneer ik als kloon start
ga naar x: (160) y: (160)
verschijn
herhaal (22) 
  verander y met (-4)
end
herhaal (170) 
  verander x met (-2)
  draai tegen de klok in (6) graden
end
herhaal (30) 
  verander y met (-4)
end
herhaal (180) 
  verander x met (2)
  draai met de klok mee (6) graden
end
herhaal (30) 
  verander y met (-4)
end
herhaal (170) 
  verander x met (-2)
  draai tegen de klok in (6) graden
end
verwijder deze kloon
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \----

Voeg nu een aantal codeblokken toe om een bericht te verzenden als je personage wordt geraakt door een bal!

Voeg deze code toe aan je balsprite:

![balsprite](images/ball_sprite.png)

```blocks3
    wanneer ik als kloon start
  herhaal 
    als < raak ik (Pico loopt v)? > dan
            zend signaal (raak v)
        end
    end
```

\--- /task \---

\--- task \---

Voeg ten slotte code-blokken toe aan jouw personagesprite om terug te gaan naar de beginpositie wanneer deze de `raak` boodschap ontvangt:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    wanneer ik signaal [raak v] ontvang
  richt naar (90 v) graden
  ga naar x: (-210) y: (-120)
```

\--- /task \---

\--- task \----

Test je code. Controleer of het personage teruggaat naar de start na het aanraken van een bal.

\--- /task \---