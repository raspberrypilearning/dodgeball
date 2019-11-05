## Reto: Más obstáculos

Si crees que tu juego es demasiado fácil puedes poner más obstáculos. ¡Los obstáculos pueden ser lo que quieras! Aquí tienes algunas sugerencias:

+ Una mariposa peligrosa
+ Plataformas que aparecen y desaparecen
+ Pelotas de tenis cayendo que deben esquivarse

![captura de pantalla](images/dodge-obstacles.png)

Incluso podrías diseñar otro fondo para crear el siguiente nivel. Deespués añade código para que cuando tu personaje llegue a la puerta verde el juego cambie al nuevo fondo:

![objeto de pico caminando](images/pico_walking_sprite.png)

```blocks3
    si <touching color [#00FF00]?> entonces
        cambiar fondo a (siguiente fondo v)
        ir a x: (-210) y: (-120)
        esperar (1) segundos
    final
```