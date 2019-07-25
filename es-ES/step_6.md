## Esquivar los balones

Tu personaje puede moverse y saltar ahora, así que es hora de agregar algunas bolas que el personaje debe evitar.

\--- task \---

Crea un nuevo sprite de bolas. Puedes elegir cualquier tipo de balón que te guste.

![captura de pantalla](images/dodge-balls.png)

\--- /task \---

\--- task \---

Cambiar el tamaño de la bola sprite para que el personaje puede saltar sobre él. Intenta hacer que el personaje salte sobre la bola para comprobar si la bola tiene el tamaño correcto.

![captura de pantalla](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Añade este código a tu bola sprite:

![bola sprite](images/ball_sprite.png)

```blocks3
cuando se hace clic en la bandera verde
ocultar
para siempre 
  espere (3) segundos
  cree un clon de (yo v)
final
```

```blocks3
cuando comience como un clon
vaya a x: (160) y: (160)
muestre
repetición (22) 
  cambie y por (-4)
final
repita (170) 
  cambie x por (-2)
  gire ccw (6) grados
fin
repita (30) 
  cambie y por (-4)
fin
borre este clon
```

Este código crea un nuevo clon del sprite de bola cada tres segundos. Cada nuevo clon se mueve a lo largo de la plataforma superior y luego cae.

\--- /task \---

\--- task \---

Haga clic en la bandera para probar el juego.

![captura de pantalla](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Agrega más código a tu sprit de bola para que los clones se muevan a través de las tres plataformas.

![captura de pantalla](images/dodge-ball-more-motion.png)

\--- consejos \---

\--- hint \---

Repita los bloques de código que utilizó para mover el clon de sprite de bola a través de la primera plataforma. Debe cambiar los números `x`{: class = "block3motion"}, `y`{: class = "block3motion"}, y `repetir`{: class = "block3control"} para que los clones sigan las plataformas correctamente .

\--- /hint \---

\--- hint \---

Estos son los bloques que necesitas. Asegúrate de agregarlos en el orden correcto.

![bola sprite](images/ball_sprite.png)

```blocks3
repetir (170) 
  cambiar x por (-2)
  giro ccw (6) grados
finalizar

repetir (180) 
  cambiar x por (2)
  girar cw (6) grados
finalizar

repetir (30) 
  cambiar y por (-4)
final
```

\--- /hint \---

\--- hint \---

El código para tus clones de sprites de bola debería verse así:

![bola sprite](images/ball_sprite.png)

```blocks3
cuando comience como un clon
vaya a x: (160) y: (160)
muestre
repetición (22) 
  cambie y por (-4)
final
repita (170) 
  cambie x por (-2)
  gire ccw (6) grados
final
repita (30) 
  cambie y por (-4)
final
repita (180) 
  cambie x por (2)
  gire cw (6) grados
final
repita (30) 
  cambia y por (-4)
final
repite (170) 
  cambia x por (-2)
  gira ccw (6) grados
final
borra este clon
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

¡Ahora agregue algunos bloques de código para transmitir (enviar) un mensaje si su personaje es golpeado por una bola!

Añade este código a tu bola sprite:

![bola sprite](images/ball_sprite.png)

```blocks3
    cuando comienzo como clon
    para siempre
        si < tocan (Pico walking v)? > luego
            transmisión (hit v)
        final
    final
```

\--- /task \---

\--- task \---

Finalmente, agregue bloques de código a su sprite de personaje para que vuelva a su posición inicial cuando reciba el mensaje `hit`:

![pico caminando sprite](images/pico_walking_sprite.png)

```blocks3
    cuando recibo [golpe v]
    puntos en la dirección (90)
    vaya a x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Prueba tu código. Comprueba si el personaje vuelve al inicio después de tocar una bola.

\--- /task \---