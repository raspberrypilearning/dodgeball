## Mouvement du personnage

Commencez par créer un personnage qui peut se déplacer à gauche et à droite, et qui peut gravir des échelles.

\--- task \---

Ouvrez le projet de démarrage 'Dodgeball' Scratch.

**En ligne:** ouvre le projet de démarrage à [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on){:target="_ blank"}.

Si tu as un compte Scratch, tu peux en créer une copie en cliquant sur **Remix**.

**Offline:** téléchargez le projet de démarrage à partir de [rpf.io/p/en/dodgeball-get](http://rpf.io/p/en/dodgeball-get) , puis ouvrez-le à l'aide de l'éditeur hors ligne.

\--- /task \---

Le projet contient un fond avec des plateformes:

![fond de projet dodgeball](images/dodge-background.png)

\--- task \---

Choisissez un nouveau sprite en tant que personnage que le joueur contrôlera et ajoutez-le à votre projet. Il est préférable que vous choisissiez un sprite avec plusieurs costumes, afin de lui donner l’impression de marcher.

![choisir un sprite](images/dodge-characters.png)

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Ajoutez des blocs de code à votre image-objet afin que le joueur puisse utiliser les touches fléchées pour déplacer le personnage. Lorsque le joueur appuie sur la flèche droite, le personnage doit pointer vers la droite, faire quelques pas et passer au costume suivant:

![pico marche sprite](images/pico_walking_sprite.png)

```blocks3
lorsque le drapeau a cliqué sur
pour toujours
    si la touche <(flèche droite v) est enfoncée? > puis
        point en direction (90 v)
        déplacer (3) étapes
        costume suivant
    fin
fin
```

\--- /task \---

\--- task \---

Si votre sprite ne correspond pas, ajustez sa taille.

![définir la taille de l'image-objet pour qu'elle tienne](images/dodge-sprite-size-annotated.png)

\--- /task \---

\--- task \---

Testez votre personnage en cliquant sur le drapeau, puis en maintenant la touche flèche droite. Votre personnage se déplace-t-il vers la droite? Votre personnage a-t-il l'air de marcher?

![capture d'écran](images/dodge-walking.png)

\--- /task \---

\--- task \---

Ajoutez des blocs de code à la boucle `pour toujours`{: class = "block3control"} de l'image-objet du personnage de sorte qu'elle se déplace vers la gauche si vous appuyez sur la touche fléchée gauche.

\--- hints \---

\--- hint \---

Pour que votre personnage puisse se déplacer vers la gauche, vous devrez ajouter un autre bloc `si`{: class = "block3control"} à l'intérieur de la boucle `forever`{: class = "block3control"}. Dans ce nouveau bloc `if`{: class = "block3control"}, ajoutez du code pour que votre sprite de personnage `déplace de`{: class = "block3motion"} vers la gauche.

\--- /hint \---

\--- hint \---

Copiez le code que vous avez créé pour faire marcher le personnage à droite. Définissez ensuite la touche `appuyée`{: class = "block3sensing"} sur la flèche `gauche`{: class = "block3sensing"}, puis modifiez le `sens`{: class = "block3motion"} en `-90`.

```blocks3
si la touche <(flèche droite v) est enfoncée? > puis
    point en direction (90 v)
    déplacer (3) étapes
    costume suivant
fin
```

\--- /hint \---

\--- hint \---

Votre code devrait ressembler à ceci maintenant:

![pico marche sprite](images/pico_walking_sprite.png)

```blocks3
lorsque le drapeau vert a cliqué
pour toujours 
  si <key (right arrow v) pressed?> puis 
    points dans la direction (90 v)
    déplacements (3) étapes
    suivant costume
  fin
  si <key (left arrow v) pressed?> puis 
    points dans la direction (-90 v)
    déplacements (3) étapes
    suivants costume
  fin
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Testez votre nouveau code pour vous assurer qu'il fonctionne. Votre personnage se retourne-t-il en marchant vers la gauche?

![capture d'écran](images/dodge-upside-down.png)

Si c'est le cas, vous pouvez résoudre ce problème en cliquant sur **direction** de votre sprite de personnage, puis en cliquant sur la flèche gauche-droite.

![capture d'écran](images/dodge-left-right-annotated.png)

Ou si vous préférez, vous pouvez également résoudre le problème en ajoutant ce bloc au début du script de votre personnage:

```blocks3
définir le style de rotation [gauche-droite v]
```

\--- /task \---

\--- task \---

Pour gravir une échelle rose, l’image-objet de votre personnage doit faire quelques pas vers le haut sur la scène chaque fois que vous appuyez sur les flèches vers le haut **et** le personnage touche la bonne couleur.

Ajoutez à l'intérieur du `pour toujours votre personnage`{: class = "block3control"} boucle en `change`{: class = "block3motion"} les `y` (verticales) positions du personnage `si`{: class = "block3control"} les `la flèche vers le haut est enfoncée`{: class = "block3sensing"} et le caractère correspond à `touche la couleur rose`{: class = "block3sensing"}.

![pico marche sprite](images/pico_walking_sprite.png)

```blocks3
    si < <key (up arrow v) pressed?> et <touching color [#FF69B4]?> > alors
        changent y de (4)
    fin
```

\--- /task \---

\--- task \---

Teste ton code. Pouvez-vous faire monter le personnage sur les échelles roses et atteindre la fin du niveau?

![capture d'écran](images/dodge-test-character.png)

\--- /task \---