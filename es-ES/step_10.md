--- challenge ---
## Reto: Gravedad mejorada 
Hay otro pequeño error en el juego: la gravedad no funciona si _cualquier_ parte de tu personaje está tocando una plataforma azul, ¡incluso su cabeza!. Puedes comprobarlo si haces subir al personaje casi hasta arriba de un poste y después lo mueves hacia la izquierda.

![screenshot](images/dodge-gravity-bug.png)

¿Puedes arreglar este error? Para hacerlo, tienes que cambiar el color de los pantalones del personaje (en _todos_ los disfraces)...

![screenshot](images/dodge-trousers.png)

...y a continuación sustituir el código:

```blocks
	< ¿tocando el color [#0000FF]? >
```

por:

```blocks
	< ¿color [#00FF00] tocando [#0000FF]? >
```

¡Recuerda probar estas mejoras para asegurarte de que has arreglado el error!



--- /challenge ---