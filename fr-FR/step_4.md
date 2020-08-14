## Gravité et saut

Tu vas maintenant faire bouger ton personnage de façon plus réaliste : tu vas ajouter de la gravité à ton jeu et lui donner la possibilité de sauter.

--- task ---

Dans le jeu, déplace ton personnage pour qu’il sorte d’une plate-forme. Est-ce que tu vois qu'il peut marcher dans un espace vide ?

![capture d'écran](images/dodge-no-gravity.png)

--- /task ---

--- task ---

Pour résoudre ce problème, ajoute de la gravité à ton jeu. Pour ce faire, crée une nouvelle variable appelée `gravité`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

Tu peux cacher cette variable de ta scène si tu le souhaites.

![capture d'écran](images/dodge-gravity-annotated.png)

--- /task ---

--- task ---

Ajoute ces nouveaux blocs de code qui définissent la `gravité` à un nombre négatif et utilise la valeur `gravité` pour modifier de manière répétée les coordonnées y de ton personnage :

![sprite pico walking](images/pico_walking_sprite.png)

```blocks3
	when flag clicked
	set [gravité v] to [-4]
	forever
		change y by (gravité)
	end
```

--- /task ---

--- task ---

Clique sur le drapeau, puis fait glisser ton personnage vers le haut de la scène. Que se passe-t-il ? La gravité fonctionne-t-elle comme prévu ?

![capture d'écran](images/dodge-gravity-drag.png)

--- /task ---

--- task ---

La gravité ne devrait pas déplacer le sprite du personnage à travers une plate-forme ou une échelle ! Ajoute un bloc `si`{:class="block3control"} à ton code pour que la gravité ne fonctionne que lorsque le personnage est en plein vol. Le code de gravité devrait alors ressembler à ceci :

![sprite pico walking](images/pico_walking_sprite.png)

```blocks3
	when flag clicked
	set [gravité v] to [-4]
	forever
		if < not < <touching color [#0000FF]?> or <touching color [#FF69B4]?> > > then
			change y by (gravité)
		end
	end
```

--- /task ---

--- task ---

Teste à nouveau le jeu pour voir si la gravité fonctionne correctement maintenant. Est-ce que ton sprite de personnage arrête de tomber quand il touche une plate-forme ou une échelle ? Peux-tu faire marcher le personnage sur le bord des plates-formes et tomber au niveau inférieur ?

![capture d'écran](images/dodge-gravity-test.png)

--- /task ---

--- task ---

Ajoute maintenant du code pour que ton personnage saute chaque fois que le joueur appuie sur la touche <kbd>espace</kbd>. Un moyen très simple de faire cela est de déplacer ton personnage plusieurs fois :

![sprite pico walking](images/pico_walking_sprite.png)

```blocks3
	when [space v] key pressed
	repeat (10)
		change y by (4)
	end
```

Parce que la gravité pousse constamment ton personnage vers le bas de 4 pixels, tu dois choisir un nombre plus grand que `4` dans ton bloc `mettre (4) à y`{:class="block3motion"}. Change le nombre jusqu'à ce que tu sois satisfait de la hauteur à laquelle le personnage saute.

--- /task ---

--- task ---

Teste ton code. Note que le mouvement de saut n'est pas très fluide. Pour rendre le saut plus fluide, tu dois déplacer ton sprite de personnage par des distances de plus en plus petites, jusqu'à ce qu'il ne monte pas plus haut.

--- /task ---

--- task ---

Pour faire cela, crée une nouvelle variable appelée `hauteur du saut`{:class="block3variables"}. Encore une fois, tu peux cacher cette variable si tu préfères.

--- /task ---

--- task ---

Supprime le code de saut que tu as ajouté au sprite de ton personnage et ajoute ce code à la place :

![sprite pico walking](images/pico_walking_sprite.png)

```blocks3
	when [space v] key pressed
	set [hauteur du saut v] to [8]
	repeat until < (hauteur du saut) = [0] >
		change y by (hauteur du saut)
		change [hauteur du saut v] by (-0.5)
	end
```

Ce code déplace ton personnage de 8 pixels, puis de 7,5 pixels, puis de 7 pixels, et ainsi de suite, jusqu'à ce qu'il ne monte plus. Cela rend le saut plus fluide.

--- /task ---

--- task ---

Modifie la valeur de la variable `hauteur du saut`{:class="block3variables"} définie avant que les `répétitions`{:class="block3control"} commencent. Teste ensuite ton jeu.

Répète ces deux étapes jusqu'à ce que tu sois satisfait de la hauteur de saut du personnage.

--- /task ---