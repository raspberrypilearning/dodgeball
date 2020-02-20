## Défi : plus d'obstacles

Si tu penses que ton jeu est encore trop facile, tu peux lui ajouter plus d'obstacles. Les obstacles peuvent être tout ce que tu veux ! Voici quelques idées :

+ Un papillon dangereux
+ Des plateformes qui apparaissent et disparaissent
+ Chutes de balles de tennis à éviter

![capture d'écran](images/dodge-obstacles.png)

Tu peux même concevoir un autre fond pour créer le niveau suivant. Ajoute ensuite du code pour que, lorsque ton personnage atteint la porte verte, le jeu bascule vers le nouvel arrière-plan :

![sprite pico walking](images/pico_walking_sprite.png)

```blocks3
    si <touching color [#00FF00]?> alors
        basculer sur le fond (fond suivant v)
        allez à x: (-210) y: (-120)
        attendre (1) seconde
    fin
```