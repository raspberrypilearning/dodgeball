## Lasers!

Pour votre jeu un peu plus difficile à compléter, vous allez ajouter des lasers!

\--- task \---

Ajoutez un nouveau sprite à votre jeu et appelez-le `laser`. Il devrait avoir deux costumes: l'un appelé "on" et l'autre appelé "off".

![capture d'écran](images/dodge-lasers-costume1.png)

![capture d'écran](images/dodge-lasers-costume2.png)

\--- /task \---

\--- task \---

Placez votre nouveau sprite laser entre deux plates-formes.

![capture d'écran](images/dodge-lasers-position.png)

\--- /task \---

\--- task \---

Ajoutez du code à votre sprite laser pour le faire basculer entre ses deux costumes.

![sprite laser](images/laser_sprite.png)

```blocks3
    lorsque le drapeau est cliqué
    pour toujours
        changer de costume en (sur v)
        attendre (2) secondes
        changer de costume en (off v)
        attendre (2)
    secondes
```

Si vous préférez, vous pouvez modifier le code présenté ci-dessus de sorte que l'image-objet `attend`{: class = "block3control"} un `aléatoire`{: class = "block3operators"} durée entre les changements de costume.

\--- /task \---

\--- task \---

Enfin, ajoutez du code à votre image-objet laser afin que celle-ci diffuse un message de «hit» lorsqu'elle touche l'image-objet du personnage.

\--- hints \---

\--- hint \---

Ce code doit être très similaire au code que vous avez ajouté à votre sprite boule.

\--- /hint \---

\--- hint \---

Copiez le code que vous avez ajouté à l'image-objet balle pour que cette image-objet `diffuse 'hit'`': {class = "block3control"} lorsqu'il touche `à votre personnage`{: class = "block3sensing"}.

\--- /hint \---

\--- hint \---

C'est le code que vous devriez ajouter:

![sprite laser](images/laser_sprite.png)

```blocks3
lorsque le drapeau vert a cliqué sur
pour toujours 
  si <touching (Pico walking v) ?> puis 
    diffusion (hit v)
  end
end
```

\--- /hint \---

\--- /hints \---

Vous n'avez pas besoin d'ajouter de code supplémentaire au sprite de votre personnage, car celui-ci sait déjà quoi faire lorsqu'il reçoit la diffusion `diffusion 'hit'`{: class = "block3control"}!

\--- /task \---

\--- task \---

Testez votre jeu pour voir si vous pouvez déplacer le personnage au-delà du laser. Si le laser est trop facile ou trop difficile à éviter, changez les temps d'attente `{`: class = "block3control"} dans le code de l'image-objet laser.

\--- /task \---