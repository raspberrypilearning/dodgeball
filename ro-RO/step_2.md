## Cinematica personajului

Începeți prin a crea un personaj care se poate deplasa spre stânga și spre dreapta și poate urca pe scări.

\--- proba\---

Deschideți proiectul Starter Scratch "Dodgeball".

**Online:** deschideți proiectul starter la [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){: target = "_ blank"}.

Dacă ai un cont Scratch, poți să creezi o copie dând click pe **Remix**.

**Offline:** download the starter project from [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get) and then open it using the offline editor.

\--- /proba\---

The project contains a backdrop with platforms:

![dodgeball project background](images/dodge-background.png)

\--- task \---

Choose a new sprite as the character the player will control, and add it to your project. It's best if you choose a sprite with multiple costumes, so that you can make it look as though it's walking.

![pick a sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Add code blocks to your character sprite so that the player can use the arrow keys to move the character around. When the player presses the right arrow, the character should point right, move a few steps, and change to the next costume:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
când steagul a dat clic
pentru totdeauna
    dacă tasta <(săgeata la dreapta v) a fost apăsată? > apoi
        punct în direcție (90 v)
        mișcare (3) trepte
        costum următor
    capăt
capăt
```

\--- /task \---

\--- task \---

If your sprite doesn't fit, adjust its size.

![set sprite size so it fits](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Testați caracterul dvs. făcând clic pe steag și apoi ținând apăsată tasta săgeată dreapta. Does your character move to the right? Does your character look like it is walking?

![captură de ecran](images/dodge-walking.png)

\--- /task \---

\--- task \---

Add code blocks to the character sprite's `forever`{:class="block3control"} loop so that it walks left if the left arrow key is pressed.

\--- sugestii \---

\--- indiciu \---

So that your character can move to the left, you'll need to add another `if`{:class="block3control"} block inside the `forever`{:class="block3control"} loop. In this new `if`{:class="block3control"} block, add code to make your character sprite `move`{:class="block3motion"} to the left.

\--- / indiciu \---

\--- indiciu \---

Copy the code you created to make the character walk to the right. Then set the `key pressed`{:class="block3sensing"} to the `left arrow`{:class="block3sensing"}, and change the `direction`{:class="block3motion"} to `-90`.

```blocks3
dacă apăsați tasta <(săgeata dreapta v)? > apoi
    punct în direcție (90 v)
    mișcare (3) trepte
    costum următor
capăt
```

\--- / indiciu \---

\--- indiciu \---

Your code should look like this now:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
când steagul verde apasat
pentru totdeauna 
  dacă <key (right arrow v) pressed?> , apoi 
    punct în direcția (90 v)
    mutare (3) pașii
    costum următor
  capăt
  dacă <key (left arrow v) pressed?> atunci 
    punct în direcția (-90 v)
    mutare (3) pașii
    next costum
  sfârșitul
sfârșitul
```

\--- / indiciu \---

\--- / sugestii \---

\--- /task \---

\--- task \---

Testați noul cod pentru a vă asigura că funcționează. Personajul tău se răstoarnă când merge la stânga?

![captură de ecran](images/dodge-upside-down.png)

If so, you can fix this by clicking on the **direction** of your character sprite, and then clicking on the left-right arrow.

![captură de ecran](images/dodge-left-right-annotated.png)

Or if you prefer, you can also fix the problem by adding this block to the start of your character's script:

```blocks3
setati modul de rotatie [left-right v]
```

\--- /task \---

\--- task \---

To climb a pink ladder, your character sprite should move a few steps upwards on the Stage whenever the up arrow is pressed **and** the character is touching the correct colour.

Add inside your character's `forever`{:class="block3control"} loop to `change`{:class="block3motion"} the character's `y` (vertical) position `if`{:class="block3control"} the `up arrow is pressed`{:class="block3sensing"} and the character is `touching the colour pink`{:class="block3sensing"}.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if < <key (up arrow v) pressed?> and <touching color [#FF69B4]?> > then
        change y by (4)
    end
```

\--- /task \---

\--- task \---

Test your code. Can you make the character climb the pink ladders and get to the end of the level?

![captură de ecran](images/dodge-test-character.png)

\--- /task \---