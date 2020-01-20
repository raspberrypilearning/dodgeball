## Esquive des balles

Votre personnage peut maintenant se déplacer et sauter, il est donc temps d'ajouter quelques balles que le personnage doit éviter.

\--- task \---

Créer un nouveau sprite de balle. Vous pouvez choisir n'importe quel type de balle que vous aimez.

![capture d'écran](images/dodge-balls.png)

\--- /task \---

\--- task \---

Redimensionnez le sprite de la balle afin que le personnage puisse sauter par-dessus. Essayez de faire sauter le personnage par-dessus le ballon pour vérifier si le ballon a la bonne taille.

![screenshot](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Ajoutez ce code à votre sprite boule:

![balle sprite](images/ball_sprite.png)

```blocks3
lorsque le drapeau vert a cliqué
masquer
pour toujours 
  attendre (3) secondes
  créer un clone de (moi v)
fin
```

```blocks3
quand je commence comme clone
aller à x: (160) y: (160)
montrer
répéter (22) 
  changer y par (-4)
fin
répéter (170) 
  changer x par (-2)
  tourner ccw (6) degrés
fin
répétition (30) 
  changer y par (-4)
fin
supprimer ce clone
```

Ce code crée un nouveau clone du sprite balle toutes les trois secondes. Chaque nouveau clone se déplace le long de la plate-forme supérieure, puis tombe.

\--- /task \---

\--- task \---

Cliquez sur le drapeau pour tester le jeu.

![capture d'écran](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Ajoutez plus de code à votre image-objet balle afin que ses clones se déplacent sur les trois plates-formes.

![capture d'écran](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Répétez les blocs de code que vous avez utilisés pour déplacer le clone de sprite boule sur la première plate-forme. Vous devez modifier les nombres `x`{: class = "block3motion"}, `y`{: class = "block3motion"} et `répéter`{: class = "block3control"} pour que les clones suivent correctement les plates-formes. .

\--- /hint \---

\--- hint \---

Ce sont les blocs dont vous avez besoin. Assurez-vous de les ajouter dans le bon ordre.

![balle sprite](images/ball_sprite.png)

```blocks3
répéter (170) 
  changer x par (-2)
  tour par tour (6)
fin

répéter (180) 
  changer x par (2)
  tourner de gauche à droite (6) degrés
fin

répéter (30) 
  changer y par (-4)
fin
```

\--- /hint \---

\--- hint \---

Le code de votre clone de sprite balle devrait ressembler à ceci:

![balle sprite](images/ball_sprite.png)

```blocks3
quand je commence en tant que clone
aller à x: (160) y: (160)
montrer
répéter (22) 
  changer y par (-4)
fin
répéter (170) 
  changer x par (-2)
  tournez ccw (6)
fin
répétez (30) 
  changez y par (-4)
fin
répétez (180) 
  changez x (2)
  tournez (6) degrés
fin
répétez (30) 
  changer y de (-4)
fin
répéter (170) 
  changer x de (-2)
  virage ccw (6) degrés
fin
supprimer ce clone
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Ajoutez maintenant quelques blocs de code pour diffuser (envoyer) un message si votre personnage est touché par une balle!

Ajoutez ce code à votre sprite boule:

![balle sprite](images/ball_sprite.png)

```blocks3
    quand je commence comme un clone
    pour toujours
        si < touchants (Pico walking v)? > puis
            diffusion (hit v)
        end
    end
```

\--- /task \---

\--- task \---

Enfin, ajoutez des blocs de code au sprite de votre personnage pour le ramener à sa position de départ lorsqu'il reçoit le message `hit`:

![pico marche sprite](images/pico_walking_sprite.png)

```blocks3
    quand je reçois [hit v]
    point en direction (90)
    aller à x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Testez votre code. Vérifiez si le personnage revient au début après avoir touché une balle.

\--- /task \---