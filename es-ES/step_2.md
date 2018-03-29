## Movimientos del personaje

Empezaremos por crear un personaje que pueda moverse hacia la derecha y la izquierda, y que pueda subirse a postes.

+ Crea un nuevo proyecto de Scratch y borra el objeto gato para que el proyecto esté vacío. Puedes encontrar el editor online de Scratch en <a href="http://jumpto.cc/scratch-new">jumpto.cc/scratch-new</a>.

+ Para este proyecto, deberías de tener una carpeta llamada 'Recursos del Proyecto', en la que encontrarás la imagen de fondo que necesitas. Asegúrate de que tienes esta carpeta, y pregunta al líder del Club si no la encuentras.

	![screenshot](images/dodge-resources.png)

+ Carga la imagen 'background.png' como nuevo escenario. ¡También puedes añadir un dibujo que hayas hecho tú! Si vas a dibujar tu propio nivel, asegúrate de que los postes y las plataformas son de colores diferentes, y de que haya una puerta (o algo parecido) a la que el jugador tenga que llegar. Tu proyecto debería parecerse a éste:

	![screenshot](images/dodge-background.png)

+ Añade un nuevo objeto, que será tu personaje. Es mejor que escojas un objeto que tenga varios disfraces, así podrás crear el efecto de que está caminando.

	![screenshot](images/dodge-characters.png)

+ Usaremos las flechas del teclado para que el personaje se mueva en diferentes direcciones. Cuando el jugador pulse la flecha derecha, queremos que el personaje mire hacia la derecha, dé unos pasos en esa dirección y cambie al siguiente disfraz:

	```blocks
		al presionar bandera verde
		por siempre
			si <¿tecla [flecha derecha v] presionada?> entonces
				apuntar en dirección (90 v)
				mover (3) pasos
				siguiente disfraz
			fin
		fin
	```

+ Haz una prueba presionando la bandera y a continuación manteniendo pulsada la tecla derecha. ¿Se mueve el personaje hacia la derecha? ¿Parece que el personaje está caminando?

	![screenshot](images/dodge-walking.png)

+ Para que el personaje se mueva hacia la izquierda, tendrás que añadir otro bloque `si`{:class="blockcontrol"} dentro del bucle `por siempre`{:class="blockcontrol"}. ¡Recuerda probar el nuevo código para asegurarte de que funciona!

+ Para subirse a un poste, tu personaje debería moverse un poco hacia arriba siempre que se pulse la flecha arriba y esté tocando el color correcto. Añade este código al bucle `por siempre`{:class="blockcontrol"} de tu personaje:

	```blocks
		si <<¿tecla [flecha arriba v] presionada?> y <¿tocando el color [#FFFF00]?>> entonces
			cambiar y por (4)
		fin
	```

+ Prueba los movimientos de tu personaje: ¿Puedes subirte a los postes amarillos y llegar al final del nivel?

	![screenshot](images/dodge-test-character.png)
