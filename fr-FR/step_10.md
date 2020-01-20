## Défi : gravité améliorée

Il y a un autre petit bug dans votre jeu: la gravité ne tire pas les bas du personnage si **tout** partie de l'image - objet est en contact avec une plate - forme bleue. Donc, même si la tête du sprite touche une plate-forme, le sprite ne tombe pas! Vous pouvez le tester vous-même: faites grimper votre personnage le plus haut possible, puis déplacez-le latéralement sous une plate-forme:

![capture d'écran](images/dodge-gravity-bug.png)

Pour résoudre ce problème, vous devez d’abord donner à votre personnage un nouveau pantalon de couleur différente (sur **costumes**).

![capture d'écran](images/dodge-trousers.png)

Puis remplacez ce bloc de code:

```blocks3
    < couleur touchante [# 0000FF]? >
```

avec ce bloc de code:

```blocks3
    < couleur [# 00FF00] est en contact avec [# 0000FF]? >
```

Pour vous assurer que vous avez corrigé le bogue, testez le jeu après avoir apporté ces modifications!