## Lasers!

Rendez votre jeu un peu plus compliqué en ajoutant des lasers!

+ Ajoutez un nouveau lutin appelé 'Laser' à votre jeu. Il devrait avoir 2 costumes appelés 'on' et 'off'.

	![screenshot](images/dodge-lasers-costume.png)

+ Placez votre nouveau laser n'importe où entre 2 plateformes.

	![screenshot](images/dodge-lasers-position.png)

+ Ajoutez le code à votre laser pour qu'il puisse changer entre les 2 costumes.

	```blocks
		quand le drapeau vert pressé
		répéter indéfiniment
			basculer sur le costume [Activé v]
			attendre (2) secondes
			basculer sur le costume [Désactivé v]
			attendre (2) secondes
		end
	```

	Si vous préférez, vous pouvez `Attendre`{:class="blockcontrol"} un temps `aléatoire`{:class="blockoperators"} entre les changements de costume.

+ Finalement, ajoutez le code à votre laser pour que le message 'hit' soit diffusé quand le laser touche votre personnage. Ce code sera le même que vous avez ajouté à votre lutin de balle.

	Vous n'avez pas à ajouter plus de codes à votre personnage, il sait déjà quoi faire lorsqu'il est frappé!

+ Testez votre jeu pour voir si vous pouvez arriver devant le laser. Changer le temps `attendre`{:class="blockcontrol"} dans votre code si les lasers sont trop faciles ou trop difficiles.
