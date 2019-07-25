## Reto: Más obstáculos

Si crees que tu juego es demasiado fácil, puedes agregarle más obstáculos. ¡Los obstáculos pueden ser lo que quieras! Aquí tienes algunas sugerencias:

+ Una mariposa peligrosa
+ Plataformas que aparecen y desaparecen.
+ Pelotas de tenis en caída que deben evitarse.

![captura de pantalla](images/dodge-obstacles.png)

Incluso podrías diseñar otro fondo para crear el siguiente nivel. Luego agrega código para que, cuando tu personaje llegue a la puerta verde, el juego cambie al nuevo fondo:

![pico caminando sprite](images/pico_walking_sprite.png)

```blocks3
    si <touching color [#00FF00]?> entonces
        cambia el telón de fondo a (el siguiente telón de fondo v)
        va a x: (-210) y: (-120)
        espera (1) segundos
    fin
```