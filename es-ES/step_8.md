## ¡Láseres!

A tu juego, un poco más difícil de completar, ¡vas a agregar láseres!

\--- task \---

Agrega un nuevo sprite a tu juego y llámalo `láser`. Debe tener dos disfraces: uno llamado 'on' y otro llamado 'off'.

![captura de pantalla](images/dodge-lasers-costume1.png)

![screenshot](images/dodge-lasers-costume1.png)

\--- /task \---

\--- task \---

Coloca tu nuevo sprite láser entre dos plataformas.

![captura de pantalla](images/dodge-lasers-position.png)

\--- /task \---

\--- task \---

Agrega código a tu sprite láser para que cambie entre sus dos disfraces.

![sprite láser](images/laser_sprite.png)

```blocks3
    cuando la bandera haga clic en
    para siempre
        cambie el traje a (en v)
        espere (2) segundos
        cambie el traje a (apagado v)
        espere (2) segundos
    fin
```

Si lo prefieres, puedes cambiar el código que se muestra arriba para que el sprite `espere`{: class = "block3control"} a `aleatorios`{: class = "block3operators"} de tiempo entre los cambios de vestuario.

\--- /task \---

\--- task \---

Finalmente, agregue código a su sprite láser para que el sprite láser emita un mensaje de "éxito" cuando toque el sprite de carácter.

\--- consejos \---

\--- hint \---

Este código debe ser muy similar al código que agregó a su sprite ball.

\--- /hint \---

\--- hint \---

Copia el código que agregas a la bola sprite para hacer que la transmisión de este sprite `'hit'`{: class = "block3control"} cuando es `tocar tu personaje`{: class = "block3sensing"}.

\--- /hint \---

\--- hint \---

Este es el código que debes agregar:

![sprite láser](images/laser_sprite.png)

```blocks3
cuando la bandera verde hizo clic en
para siempre 
  si <touching (Pico walking v) ?> luego 
    emitió (golpeó v)
  final
final
```

\--- /hint \---

\--- /hints \---

No es necesario que agregue ningún código adicional a su sprite de caracteres, porque el sprite de caracteres ya sabe qué hacer cuando recibe la emisión `'hit'`{: class = "block3control"}!

\--- /task \---

\--- task \---

Prueba tu juego para ver si puedes mover al personaje más allá del láser. Si el láser es demasiado fácil o demasiado difícil de evitar, cambiar las `de espera`{: class = "block3control"} veces en el código para el sprite láser.

\--- /task \---