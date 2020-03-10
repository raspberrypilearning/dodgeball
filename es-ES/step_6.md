## Esquivando las pelotas

Tu personaje ya puede moverse y saltar, así que es hora de agregar algunas pelotas que el personaje debe evitar.

--- task ---

Crea un nuevo objeto para la pelota. Puedes elegir cualquier tipo de pelota que te guste.

![captura de pantalla](images/dodge-balls.png)

--- /task ---

--- task ---

Cambia el tamaño del objeto de la pelota para que el personaje puede saltar sobre ella. Intenta hacer que el personaje salte sobre la pelota para comprobar si tiene el tamaño correcto.

![captura de pantalla](images/dodge-ball-resize.png)

--- /task ---

--- task ---

Añade este código al objeto pelota:

![objeto pelota](images/ball_sprite.png)

```blocks3
when green flag clicked
esconder
por siempre 
  esperar (3) segundos
  crear un clon de (mí mismo v)
end
```

```blocks3
al comenzar como clon
ir a x: (160) y: (160)
mostrar
repetir (22) 
  sumar a y (-4)
end
repetir (170) 
  sumar a x (-2)
  turn ccw (6) degrees
end
repetir (30) 
  sumar a y (-4)
end
eliminar este clon
```

Este código crea un nuevo clon del objeto de la pelota cada tres segundos. Cada nuevo clon se mueve a lo largo de la plataforma superior y luego cae.

--- /task ---

--- task ---

Haz clic en la bandera verde para probar el juego.

![captura de pantalla](images/dodge-ball-test.png)

--- /task ---

--- task ---

Añade más código a tu objeto de pelota para que los clones se muevan por las tres plataformas.

![captura de pantalla](images/dodge-ball-more-motion.png)

--- hints ---


--- hint ---

Repite los bloques de código que has usado para mover el clon de la pelota por la primera plataforma. Debes cambiar los números `x`{:class="block3motion"}, `y`{:class="block3motion"} y `repetir`{:class="block3control"} para que los clones sigan las plataformas correctamente.

--- /hint ---

--- hint ---

Éstos son los bloques que necesitas. Asegúrate de colocarlos en el orden correcto.

![objeto pelota](images/ball_sprite.png)

```blocks3
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end

repeat (180) 
  change x by (2)
  turn cw (6) degrees
end

repeat (30) 
  change y by (-4)
end
```

--- /hint ---

--- hint ---

El código de tus clones del objeto de pelota debería ser algo así:

![objeto pelota](images/ball_sprite.png)

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (180) 
  change x by (2)
  turn cw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
delete this clone
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

¡Ahora añade algunos bloques de código para transmitir (enviar) un mensaje si tu personaje es golpeado por una bola!

Añade este código a tu objeto pelota:

![objeto pelota](images/ball_sprite.png)

```blocks3
    al comenzar como clon
    por siempre
        if < touching (Pico walking v)? > then
            enviar (tocado v)
        end
    end
```

--- /task ---

--- task ---

Finalmente, añade bloques de código a tu objeto de personaje para que vuelva a su posición inicial cuando reciba el mensaje `tocado`:

![objeto pico caminando](images/pico_walking_sprite.png)

```blocks3
    al recibir [tocado v]
    apuntar en dirección (90)
    ir a x: (-210) y: (-120)
```

--- /task ---

--- task ---

Prueba tu código. Comprueba si el personaje vuelve al inicio después de tocar una pelota.

--- /task ---