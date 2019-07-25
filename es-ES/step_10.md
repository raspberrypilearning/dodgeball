## Reto: Gravedad mejorada

Hay otro pequeño fallo en su juego: la gravedad no tire el sprite carácter a la baja si **ninguna** parte del sprite está en contacto con una plataforma azul. Así que incluso si la cabeza del sprites toca una plataforma, ¡el sprite no se cae! Puedes probar esto por ti mismo: haz que tu personaje suba la mayor parte del camino por una escalera y luego mueve al personaje de lado debajo de una plataforma:

![captura de pantalla](images/dodge-gravity-bug.png)

Para corregir el error, primero debes darle a tu personaje sprite nuevos pantalones que tengan un color diferente (en **todos los** disfraces).

![captura de pantalla](images/dodge-trousers.png)

Luego reemplace este bloque de código:

```blocks3
    < tocando color [# 0000FF]? >
```

con este bloque de código:

```blocks3
    < color < [# 00FF00] está tocando [# 0000FF]? >
```

¡Para asegurarte de haber solucionado el error, prueba el juego después de haber realizado estos cambios!