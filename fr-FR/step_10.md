## Défi : gravité améliorée

Il y a un autre petit bug dans ton jeu : la gravité ne pousse pas le personnage vers le bas si **une** partie du sprite touche une plate-forme bleue. Donc, même si la tête du sprite touche une plate-forme, le sprite ne tombe pas ! Tu peux le tester toi-même: fais grimper ton personnage le plus haut possible, puis déplace-le latéralement sous une plate-forme :

![capture d'écran](images/dodge-gravity-bug.png)

Pour résoudre ce problème, tu dois d’abord donner à ton personnage un nouveau pantalon de couleur différente (sur **tous** les costumes).

![capture d'écran](images/dodge-trousers.png)

Puis remplace ce bloc de code :

```blocks3
    < touching color [#0000FF]? >
```

avec ce bloc de code :

```blocks3
    < color [#00FF00] is touching [#0000FF]? >
```

Pour t'assurer que tu as corrigé le bogue, teste le jeu après avoir apporté ces modifications !