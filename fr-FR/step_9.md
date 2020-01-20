## Défi : Plus d'obstacles

Si vous pensez que votre jeu est encore trop facile, vous pouvez lui ajouter plus d'obstacles. Les obstacles peuvent être ce que vous voulez! Voici quelques idées:

+ Un papillon dangereux
+ Des plateformes qui apparaissent et disparaissent
+ Chutes de balles de tennis à éviter

![capture d'écran](images/dodge-obstacles.png)

Vous pouvez même concevoir un autre fond pour créer le niveau suivant. Ajoutez ensuite du code pour que, lorsque votre personnage atteint la porte verte, le jeu bascule vers le nouvel arrière-plan:

![pico marche sprite](images/pico_walking_sprite.png)

```blocks3
    si <touching color [#00FF00]?> alors
        change de fond en (fond suivant v)
        va à x: (-210) y: (-120)
        attend (1)
    secondes
```