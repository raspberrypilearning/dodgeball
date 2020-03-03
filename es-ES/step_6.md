## Esquivando las pelotas

Tu personaje ya puede moverse y saltar, así que es hora de agregar algunas pelotas que el personaje debe evitar.

\--- task \---

Crea un nuevo objeto para la pelota. Puedes elegir cualquier tipo de pelota que te guste.

![captura de pantalla](images/dodge-balls.png)

\--- /task \---

\--- task \---

Cambia el tamaño del objeto de la pelota para que el personaje puede saltar sobre ella. Intenta hacer que el personaje salte sobre la pelota para comprobar si tiene el tamaño correcto.

![captura de pantalla](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

Añade este código al objeto pelota:

![objeto pelota](images/ball_sprite.png)

```blocks3
al hacer clic en la bandera verde
esconder
por siempre 
  esperar (3) segundos
  crear un clon de (mí mismo v)
final
```

```blocks3
al comenzar como clon
ir a x: (160) y: (160)
mostrar
repetir (22) 
  sumar a y (-4)
final
repetir (170) 
  sumar a x (-2)
  girar en sentido antihorario (6) grados
final
repetir (30) 
  sumar a y (-4)
final
eliminar este clon
```

Este código crea un nuevo clon del objeto de la pelota cada tres segundos. Cada nuevo clon se mueve a lo largo de la plataforma superior y luego cae.

\--- /task \---

\--- task \---

Haz clic en la bandera verde para probar el juego.

![captura de pantalla](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

Añade más código a tu objeto de pelota para que los clones se muevan por las tres plataformas.

![captura de pantalla](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

Repite los bloques de código que has usado para mover el clon de la pelota por la primera plataforma. Debes cambiar los números `x`{:class="block3motion"}, `y`{:class="block3motion"} y `repetir`{:class="block3control"} para que los clones sigan las plataformas correctamente.

\--- /hint \---

\--- hint \---

Éstos son los bloques que necesitas. Asegúrate de colocarlos en el orden correcto.

![objeto pelota](images/ball_sprite.png)

```blocks3
repetir (170) 
  sumar a x (-2)
  girar en sentido antihorario (6) grados
final

repetir (180) 
  sumar a x (2)
  girar en sentido horario (6) grados
final

repetir (30) 
  sumar a y (-4)
final
```

\--- /hint \---

\--- hint \---

El código de tus clones del objeto de pelota debería ser algo así:

![objeto pelota](images/ball_sprite.png)

```blocks3
al comenzar como clon
ir a x: (160) y: (160)
mostrar
repetir (22) 
  sumar a y (-4)
final
repetir (170) 
  sumar a x (-2)
  girar en sentido antihorario (6) grados
final
repetir (30) 
  sumar a  y (-4)
final
repetir (180) 
  sumar a x (2)
  girar en sentido horario (6) grados
final
repetir (30) 
  sumar a y (-4)
final
repetir (170) 
  sumar a x (-2)
  girar en sentido antihorario (6) grados
final
eliminar este clon
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

¡Ahora añade algunos bloques de código para transmitir (enviar) un mensaje si tu personaje es golpeado por una bola!

Añade este código a tu objeto pelota:

![objeto pelota](images/ball_sprite.png)

```blocks3
    al comenzar como clon
    por siempre
        si < tocando (Pico caminando v)? > entonces
            enviar (tocado v)
        final
    final
```

\--- /task \---

\--- task \---

Finalmente, añade bloques de código a tu objeto de personaje para que vuelva a su posición inicial cuando reciba el mensaje `tocado`:

![objeto pico caminando](images/pico_walking_sprite.png)

```blocks3
    al recibir [tocado v]
    apuntar en dirección (90)
    ir a x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

Prueba tu código. Comprueba si el personaje vuelve al inicio después de tocar una pelota.

\--- /task \---