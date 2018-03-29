--- challenge ---
## Reto: Más obstáculos 
Si todavía crees que el juego es demasiado fácil, puedes añadir más obstáculos al nivel. Puedes añadir cualquier cosa, pero te damos algunas ideas:

+ Una mariposa voladora asesina;
+ Plataformas que aparecen y desaparecen;
+ Pelotas de tenis que caen y que el personaje debe evitar.

![screenshot](images/dodge-obstacles.png)

Incluso podrías crear más de un fondo, y hacer que el personaje pase al siguiente nivel cuando llega a la puerta marrón:

```blocks
	si <¿tocando el color [#714300]?> entonces
		cambiar fondo a [siguiente fondo v]
		ir a x:(-210) y:(-120)
		esperar (1) segundos
	fin
```




--- /challenge ---