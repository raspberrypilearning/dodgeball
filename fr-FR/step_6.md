## Esquive des balles

Ton personnage peut maintenant se déplacer et sauter, il est donc temps d'ajouter quelques balles que le personnage doit éviter.

\--- task \---

Créer un nouveau sprite de balle. Tu peux choisir n'importe quel type de balle que tu aimes.

![capture d'écran](images/dodge-balls.png)

\--- /task \---

\--- task \---

Redimensionne le sprite de la balle afin que le personnage puisse sauter par-dessus. Essaie de faire sauter le personnage par-dessus le ballon pour vérifier si le ballon a la bonne taille.

![capture d'écran](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Ajoute ce code à ton sprite de balle :

![sprite de balle](images/ball_sprite.png)

```blocks3
quand le drapeau vert est cliqué
cacher
répéter indéfiniment 
  attendre (3) secondes
  créer un clone de (moi-même v)
fin
```

```blocks3
quand je commence comme un clone
aller à x: (160) y: (160)
montrer
répéter (22) fois
  ajouter (-4) à y
fin
répéter (170) fois 
  ajouter (-2) à x
  tourner à gauche de (6) degrés
fin
répéter (30) fois
  ajouter (-4) à y
fin
supprimer ce clone
```

Ce code crée un nouveau clone du sprite de balle toutes les trois secondes. Chaque nouveau clone se déplace le long de la plate-forme supérieure, et ensuite tombe.

\--- /task \---

\--- task \---

Clique sur le drapeau pour tester le jeu.

![capture d'écran](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Ajoute plus de code à ton sprite de balle afin que ces clones se déplacent sur les trois plates-formes.

![capture d'écran](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Répète les blocs de code que tu as utilisés pour déplacer le clone de sprite de balle sur la première plate-forme. Tu dois modifier les nombres `x`{:class="block3motion"}, `y`{:class="block3motion"} et `répéter`{:class="block3control"} les nombres pour que les clones suivent correctement les plates-formes.

\--- /hint \---

\--- hint \---

Ce sont les blocs dont tu as besoin. Assure-toi de les ajouter dans le bon ordre.

![sprite de balle](images/ball_sprite.png)

```blocks3
répéter (170) fois
  ajouter (-2) à x
  tourner à gauche de (6) degrés
fin

répéter (180) fois
  ajouter (2) à x
  tourner à droite de (6) degrés
fin

répéter (30) fois 
  ajouter (-4) à y
fin
```

\--- /hint \---

\--- hint \---

Le code de ton clone du sprite de balle devrait ressembler à ceci :

![sprite de balle](images/ball_sprite.png)

```blocks3
quand je commence comme un clone
aller à x: (160) y: (160)
montrer
répéter (22) fois
  ajouter (-4) à y 
fin
répéter (170) fois 
  ajouter (-2) à x 
  tournez à gauche de (6) degrés
fin
répétez (30) fois
  ajouter (-4) à y
fin
répétez (180) fois
  ajouter (2) à x
  tournez à droite de (6) degrés
fin
répétez (30) fois
  ajouter (-4) à y
fin
répéter (170) fois 
  ajouter (-2) à x 
  tourner à gauche de (6) degrés
fin
supprimer ce clone
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Ajoute maintenant quelques blocs de code pour diffuser (envoyer) un message si ton personnage est touché par une balle !

Ajoute ce code à ton sprite de balle :

![sprite de balle](images/ball_sprite.png)

```blocks3
    quand je commence comme un clone
    répéter indéfiniment
        si < touche le (Pico walking v) ? > alors
            envoyer à tous (touché v)
        fin
    fin
```

\--- /task \---

\--- task \---

Enfin, ajoute des blocs de code au sprite de ton personnage pour le ramener à sa position de départ lorsqu'il reçoit le message `touché` :

![sprite pico walking](images/pico_walking_sprite.png)

```blocks3
    quand je reçois [touché v]
    s'orienter à (90)
    aller à x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Teste ton code. Vérifie si le personnage revient au début après avoir touché une balle.

\--- /task \---